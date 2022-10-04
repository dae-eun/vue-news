<template>
  <div id="app">
    <tool-bar></tool-bar>
    <transition name="slide-fade">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
import ToolBar from './components/ToolBar.vue';

export default {
  components: { ToolBar },
  Comments:{
    ToolBar,
  }
}
</script>

<style>
body{
  padding: 0;
  margin: 0;
}
a{
  color:#34495e;
  text-decoration: none;
}
a:hover{
  color:#42b883;
  text-decoration: underline;
}
a.router-link-exact-active{
  text-decoration: underline;
}
/* Router Transition */
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}
</style>
