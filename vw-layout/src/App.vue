<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div class="box ignore"></div>
    <div aspectratio> <div aspectratio-content></div> </div>

    <div aspectratio w-188-246 class="color"></div>
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

.test {
  border: 0.5px solid black;
  border-bottom-width: 4px;
  font-size: 14px;
  line-height: 20px;
  position: relative;
}
[w-188-246] {
  width: 188px;
}
.ignore {
  margin: 10px;
  background-color: red;
}
.box {
  width: 180px;
  height: 300px;
  border: 1px solid #333
}
.hairlines {
  border-bottom: 0.5px solid red;
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

[w-188-246] { aspect-ratio: '188:246'; }

</style>
