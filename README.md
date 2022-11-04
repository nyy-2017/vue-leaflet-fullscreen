# vue-leaflet-fullscreen

## Project setup
```
npm install leaflet.pm
npm install leaflet
npm install --save vue2-leaflet
npm install --save vue2-leaflet-fullscreen
```
# main.js文件里面引入如下这些配置: 
 
// 引入Leaflet对象
    import 'leaflet/dist/leaflet.css' // 引入样式文件
// 挂载到Vue上，便于全局使用，也可以单独页面中单独引用
    import * as L from 'leaflet'
    import 'leaflet.pm'
    import 'leaflet.pm/dist/leaflet.pm.css'
    Vue.L = Vue.prototype.$L = L
/* leaflet icon */
    delete L.Icon.Default.prototype._getIconUrl
    L.Icon.Default.mergeOptions({
        iconRetinaUrl: require('leaflet/dist/images/marker-icon-2x.png'),
        iconUrl: require('leaflet/dist/images/marker-icon.png'),
        shadowUrl: require('leaflet/dist/images/marker-shadow.png'),
    })

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
