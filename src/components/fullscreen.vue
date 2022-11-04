<template>
<div style="height: 100%; width: 100%">
    <l-map
      style="height: 98vh"
      :center="mapCentre"
      :zoom="mapZoom"
      :min-zoom="5"
      :max-zoom="18"
      :options="{zoomControl: false, attributionControl: false}"
      ref="map"
    >
      <!-- 图层切换 -->
      <l-control-layers position="topright" />
      <l-tilelayer
        v-for="item in tileProviders"
        :key="item.name"
        :name="item.name"
        :visible="item.visible"
        :url="item.url"
        :attribution="item.attribution"
        class="icon-rotate"
        layer-type="base"
      />
      <!-- 全屏的功能 -->
      <l-control-fullscreen position="bottomright" :options="{ title: { 'false': '全屏', 'true': '退出' }}" />

      <!-- 控制 zoom 右下角 放大缩小 -->
      <l-control-zoom position="bottomright" :zoom-in-title="zoomInTitle" :zoom-out-title="zoomOutTitle" />

    </l-map>
  </div>
</template>

<script>
import LControlFullscreen from 'vue2-leaflet-fullscreen'
import { LMap, LTileLayer, LControlZoom, LControlLayers } from 'vue2-leaflet'
export default {
  name: 'Fullscreen',
  components: {
    LMap,
    LControlZoom,
    'l-tilelayer': LTileLayer,
    LControlLayers,
    LControlFullscreen,
  },
  data () {
    return {
      mapCentre: [34.893118727783666, 104.54589843750001],
      mapZoom: 10,
      // 图层模式
      tileProviders: [
        {
          name: '行政区划图',
          visible: true,
          url: 'http://{s}.tile.osm.org/{z}/{x}/{y}.png'
        },
        {
          name: '卫星图',
          visible: false,
          url: 'https://{s}.tile.opentopomap.org/{z}/{x}/{y}.png'
        }
      ]
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
