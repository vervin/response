<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div class="box ignore"></div>
    <div aspectratio w-188-246>
      <div aspectratio-content></div>
    </div>
     <div class="example"></div> 
     <div class="my-viewport-units-using-thingie"></div>
    <!-- <router-view/> -->
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.ignone {
  margin: 10px;
}
.box {
  width: 180px;
  height: 300px;
}

[aspectratio] {
  position: relative;
}
[aspectratio]::before {
  content: "";
  display: block;
  width: 1px;
  margin-left: -1px;
  height: 0;
}
[aspectratio-content] {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
}
[w-188-246] {
  aspect-ratio: "188:246";
}
[w-188-246] {
  width: 188px;
  background-color: #f00;
}

@svg 1px-border {
  height: 2px;
  @rect {
    fill: var(--color, black);
    width: 100%;
    height: 50%;
  }
}
.example {
  border: 1px solid transparent;
  border-image: svg(1px-border param(--color #00b1ff)) 2 2 stretch;
}


.my-viewport-units-using-thingie { width: 50vmin; height: 50vmax; top: calc(50vh - 100px); left: calc(50vw - 100px); /* hack to engage viewport-units-buggyfill */ }

</style>
