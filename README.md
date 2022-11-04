# vue-leaflet-fullscreen
# 效果图1如下
<img src="@/assets/1.png">

# 效果图2如下
<img src="@/assets/2.png">

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

# leaflet常用插件
# 1、常用地图切换加载（osm、google、baidu、gaode、tianditu.etc）

https://github.com/htoooth/Leaflet.ChineseTmsProviders

# 2、切片地图加载（wmts）（支持矢量切片）

https://github.com/mylen/leaflet.TileLayer.WMTS

# 3、wms地图服务加载

https://github.com/heigeo/leaflet.wms

# 4、视窗范围框定（只容许查看和编辑给定范围地图）

https://github.com/aparshin/leaflet-boundary-canvas

# 5、地图要素显示比例尺控制（不同比例尺要素渲染）（根据屏幕坐标控制）（非常重要，常用）

https://github.com/GreenInfo-Network/L.TileLayer.PixelFilter/

# 6、卷帘对比（卷积运算）（历史对比）（非常重要）

https://github.com/digidem/leaflet-side-by-side

# 7、webGL地图要素渲染（适用于三维要素绘制）（非常重要）

https://gitlab.com/IvanSanchez/Leaflet.TileLayer.GL

# 8、快速重新渲染地图要素，动态修改地图样式（适用于矢量切片）(不用二次发布服务)（很实用）

（颜色获取） https://github.com/frogcat/leaflet-tilelayer-colorpicker

（样式调整）https://github.com/hnrchrdl/leaflet-tilelayer-colorizr

# 9、快速获取要素范围和属性信息（tootip方式）

https://github.com/consbio/Leaflet.UTFGrid

# 10、缓冲区（不推荐，存在bug，推荐使用geotools api后台生成缓冲区，需要坐标转换）

https://github.com/TolonUK/Leaflet.EdgeBuffer https://github.com/skeate/Leaflet.buffer

# 11、要素图层组加载过程数据获取（支持FeatureGroup loading和load事件）

https://github.com/Outdooractive/Leaflet.FeatureGroup.LoadEvents

# 12、地图要素移除，动态重新渲染底图（动画效果，缓冲效果）

https://gitlab.com/IvanSanchez/Leaflet.GridLayer.FadeOut

# 13、地图矢量切片服务加载和渲染（非常重要）

https://github.com/Leaflet/Leaflet.VectorGrid

（mapbox切片渲染）https://github.com/SpatialServer/Leaflet.MapboxVectorTile

（geojson格式渲染）https://github.com/mapbox/geojson-vt

# 14、常用格式地理数据加载（WKT、GeoJSON、KML、GPX、CSV、MDB、Shp等）

https://github.com/mapbox/leaflet-omnivore

https://github.com/makinacorpus/Leaflet.FileLayer

https://github.com/calvinmetcalf/leaflet.shapefile

# 15、地图WFS服务操作，数据增删改查（Inert、Update、Delete、Query、Transaction）（重中之重，WFS服务封装，结合oracle或者postgis数据库，arcgis server或者geoserver后台服务搭建）

https://github.com/Flexberry/Leaflet-WFST

存在bug，需要修改，已在github issues中为作者留言，希望尽快解决；

如果geoserver搭建服务端：

typeNS表示工作区间， typeName表示图层名称（表名一致）

# 16、自定义label标签（Marker，polygon）

https://github.com/Leaflet/Leaflet.label

# 17、自定义marker

https://github.com/marslan390/BeautifyMarker

# 18、聚合数据

https://github.com/Leaflet/Leaflet.markercluster

https://github.com/MazeMap/Leaflet.LayerGroup.Collision

https://github.com/SINTEF-9012/PruneCluster

# 19、热力图

https://github.com/Leaflet/Leaflet.heat

http://ursudio.com/webgl-heatmap-leaflet/

# 20、加载echarts图（聚合图、迁徙图、热力图）（非常实用）

https://github.com/wandergis/leaflet-echarts.git

# 21、要素编辑（面合并、分割、创建要素等）（结合leaflet.wfst）(非常实用)

https://github.com/Leaflet/Leaflet.toolbar

https://github.com/Leaflet/Leaflet.draw

https://github.com/Leaflet/Leaflet.Editable

https://github.com/codeofsumit/leaflet.pm

https://github.com/willfarrell/Leaflet.Clipper

# 22、图层切换，要素显示隐藏

https://github.com/ismyrnow/leaflet-groupedlayercontrol

# 23、地图导航条、全屏控件

https://github.com/turbo87/sidebar-v2/

https://github.com/kartena/Leaflet.Pancontrol

https://github.com/kartena/Leaflet.zoomslider

https://github.com/Leaflet/Leaflet.fullscreen

https://github.com/brunob/leaflet.fullscreen

# 24、鹰眼图

https://github.com/Norkart/Leaflet-MiniMap

# 25、测量控件

https://github.com/ljagis/leaflet-measure

# 26、控件按钮样式设置

https://github.com/CliffCloud/Leaflet.EasyButton

https://github.com/aratcliffe/Leaflet.contextmenu

# 27、地图打印插件

https://github.com/rowanwins/leaflet-easyPrint

https://github.com/Igor-Vladyka/leaflet.browser.print

# 28、定位当前位置

https://github.com/domoritz/leaflet-locatecontrol

29、坐标转换插件（与缓冲区、测量配合使用）（非常实用）

https://github.com/kartena/Proj4Leaflet

# 30、空间位置分析（非常实用）

（点是否在面内）https://github.com/kartena/Proj4Leaflet

（计算面积、距离）https://github.com/makinacorpus/Leaflet.GeometryUtil/blob/master/src/leaflet.geometryutil.js

# 31、路径分析（纠偏，地图匹配算法）

https://github.com/perliedman/leaflet-routing-machine

https://github.com/Project-OSRM/osrm-frontend

# 32、poi模糊查询

https://github.com/smeijer/leaflet-geosearch

https://github.com/perliedman/leaflet-control-geocoder

# 33、等势线、等势面

https://github.com/timwis/leaflet-choropleth


### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
