<template>
  <!--App.vueのtemplate内に記述-->
  <a-scene>
    <a-sky id="image-360" color="#0ff"></a-sky>

    <router-link to="/cylinder" tag="a-text" position="2 2.5 -2" value="cylinder" color="#fff" width="10"></router-link>
    <router-link to="/about" tag="a-text" position="2 1.5 -2" value="sphere" color="#fff" width="10"></router-link>
    <router-link to="/" tag="a-text" position="2 0.5 -2" value="box" color="#fff" width="10"></router-link>
    <router-view />

    <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>

    <a-camera position="0 1 0">
      <a-entity cursor="fuse: true; fuseTimeout: 500" position="0 0 -1" geometry="primitive: ring" scale="0.03 0.03 0.03" material="color: #000;" animation__enter="property: scale; startEvents: mouseenter; from: 0.03 0.03 0.03; to: 0.001 0.001 0.001; dur: 500" animation__leave="property: scale; startEvents: mouseleave; from: 0.001 0.001 0.001; to: 0.03 0.03 0.03; dur: 100;">
      </a-entity>
    </a-camera>
  </a-scene>
</template>

<style lang="scss">
a-text:active {
      color: #42b983;
    }
</style>
