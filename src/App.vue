<template>
  <div id="app">
    <div class="app-container">
      <!-- HEADER -->
      <AppHeader />
      <!-- MAIN -->
      <main>
        <AppAlbumsList />
      </main>
    </div>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppAlbumsList from "./components/AppAlbumsList.vue";
export default {
  name: 'App',
  components: {
    AppHeader,
    AppAlbumsList,
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";
@import "./style/variables.scss";

main {
  background-color: $app-dark-gray;
  overflow-y: auto;
  height: calc(100% - 60px);
}
</style>
