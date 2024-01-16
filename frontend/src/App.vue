<template>
  <div id="app">
    <HeaderComponent />
    <div class="container">
      <SidebarComponent />
      <MainContentComponent />
    </div>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import SidebarComponent from './components/SidebarComponent.vue';
import MainContentComponent from './components/MainContentComponent.vue';

export default {
  components: {
    HeaderComponent,
    SidebarComponent,
    MainContentComponent
  }
}
</script>

<style>
.container {
  display: flex;
}
</style>