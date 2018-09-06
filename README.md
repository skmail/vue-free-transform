# VueJS Free Transform Tool


[![NPM Version](https://img.shields.io/npm/v/vue-free-transform.svg?style=flat)](https://www.npmjs.com/package/vue-free-transform)  [![NPM Downloads](https://img.shields.io/npm/dm/vue-free-transform.svg?style=flat)](https://www.npmjs.com/package/vue-free-transform)   [![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT) [![Build Status](https://img.shields.io/travis/skmail/vue-free-transform/master.svg?style=flat)](https://travis-ci.org/skmail/vue-free-transform)    


VueJS component for resizing, dragging and rotating html elements using css transform matrix 

![VueJS free transform tool](https://raw.githubusercontent.com/skmail/vue-free-transform/master/image.png)

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

## Project setup
`yarn install vue-free-transform` or `npm install vue-free-transform --save`


### Compiles and hot-reloads for development
```
yarn run serve
```

### Compiles and minifies for production
```
yarn run build
```

### Lints and fixes files
```
yarn run lint
```
