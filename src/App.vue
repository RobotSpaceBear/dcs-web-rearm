<template>
  <div id="app">
    <nav-header class="nav-header"></nav-header>
    <rearm class="rearm-panel"></rearm>
    <div class="footer-panel">Footer</div>
  </div>
</template>

<script>

import NavHeader from './components/NavHeader';
import Rearm from './components/Rearm';

export default {
  name: 'App',
  components: {
    NavHeader, 
    Rearm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
/*  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;*/
  text-align: center;
  color: #2c3e50;
  /*margin-top: 60px;*/
  min-height: 100%;

  display: grid;
  grid-template-rows: [nav-slot] 60px [content-slot] 1fr [footer-slot] 50px;
  grid-gap: 5px;
  grid-template-areas: 
    "nav-slot"
    "content-slot"
    "footer-slot"
}
.nav-header{
  grid-area: nav-slot;
}
.rearm-panel{
  grid-area: content-slot;
}
.footer-panel{
 grid-area: footer-slot;
 background-color: lightcoral;
}

</style>
