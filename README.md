# VueJS Free Transform Tool


[![NPM Version](https://img.shields.io/npm/v/vue-free-transform.svg?style=flat)](https://www.npmjs.com/package/vue-free-transform)  [![NPM Downloads](https://img.shields.io/npm/dm/vue-free-transform.svg?style=flat)](https://www.npmjs.com/package/vue-free-transform)   [![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT) [![Build Status](https://img.shields.io/travis/skmail/vue-free-transform/master.svg?style=flat)](https://travis-ci.org/skmail/vue-free-transform)    


VueJS component for resizing, dragging and rotating html elements using css transform matrix 

![VueJS free transform tool](https://raw.githubusercontent.com/skmail/vue-free-transform/master/image.png)


## Installation
`yarn install vue-free-transform` or `npm install vue-free-transform --save`

## Demo
https://codesandbox.io/s/1jl7z9p3q
 
 
## Usage

```js
import FreeTransform from 'vue-free-transform'
```

```vue
  
<FreeTransform 
    :x="0"
    :y="0"
    :scale-x="1"
    :scale-y="1"
    :width="100"
    :height="100"
    :angle="0"
    :offset-x="0"
    :offset-y="0"
    @update="update($event)"
>
    <div class="element" :style="{width: `100px`,height: `100px`}">
        <img src="..."/>
    </div>

</FreeTransform>
```
## Optional Attributes

`selected`
`selectOn`
`styles`

| Attribute        | Description  |
| ------------- |:-------------:|
| styles      | additional styles for parent wrapper usefull for z-index|
| selected      | hide the controls when values is false    |
| selectOn |  trigger selection on `mousedown`, `click` or `dblclick` |
| aspect-ratio | enable aspect ratio resizing default (true)|
| scale-from-center | enable scale from center resizing default (true)|
                           


## Events
`onSelect`
`dblclick`
`click`
`mousedown`

## css

```css
    
    .tr-transform--active{
        position: absolute;
        z-index: 5;
    }
    
    .tr-transform__content{
        user-select: none;
    }
    .tr-transform__rotator {
        top: -45px;
        left: calc(50% - 7px);
    }

    .tr-transform__rotator,
    .tr-transform__scale-point {
        background: #fff;
        width: 15px;
        height: 15px;
        border-radius: 50%;
        position: absolute;
        box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.1);
        border: 1px solid rgba(0, 0, 0, 0.1);
        cursor: pointer;
    }

    .tr-transform__rotator:hover,
    .tr-transform__scale-point:hover {
        background: #F1F5F8;
    }

    .tr-transform__rotator:active,
    .tr-transform__scale-point:active {
        background: #DAE1E7;
    }

    .tr-transform__scale-point {

    }

    .tr-transform__scale-point--tl {
        top: -7px;
        left: -7px;
    }

    .tr-transform__scale-point--ml {
        top: calc(50% - 7px);
        left: -7px;
    }

    .tr-transform__scale-point--tr {
        left: calc(100% - 7px);
        top: -7px;
    }

    .tr-transform__scale-point--tm {
        left: calc(50% - 7px);
        top: -7px;
    }

    .tr-transform__scale-point--mr {
        left: calc(100% - 7px);
        top: calc(50% - 7px);
    }

    .tr-transform__scale-point--bl {
        left: -7px;
        top: calc(100% - 7px);
    }

    .tr-transform__scale-point--bm {
        left: calc(50% - 7px);
        top: calc(100% - 7px);
    }

    .tr-transform__scale-point--br {
        left: calc(100% - 7px);
        top: calc(100% - 7px);
    }
```


## Keyboard shortcuts
`shift` for aspect ratio resizing

`alt` for scaling from center

`shift` + `alt` scaling from center based on aspect ratio

`shift` while rotation will snap rotation using 15 degrees