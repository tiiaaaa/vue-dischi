<template>
    <div id="app">
        <HeaderAlbum/>
        <MainAlbum/>
    </div>
</template>

<script>
import HeaderAlbum from './components/HeaderAlbum.vue';
import MainAlbum from './components/MainAlbum.vue'

export default {
  name: 'App',
  components: {
    HeaderAlbum,
    MainAlbum,
  },
}
</script>

<style lang="scss">
@import '@/assets/style/style.scss';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
