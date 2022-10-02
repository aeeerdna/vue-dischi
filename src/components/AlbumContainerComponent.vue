<template>
  <div class="album-container">
    <div class="row">
      <div v-for="album in albums" :key="album.title" class="am-five-col">
        <SongComponent :info="album" />
      </div>
    </div>
  </div>
</template>

<script>
import SongComponent from "./SongComponent.vue";
export default {
  name: "AlbumContainerComponent",
  props: {
    albums: Array,
  },
  components: {
    SongComponent,
  },
};
</script>

<style lang="scss" scoped>
.album-container {
  padding-top: 50px;
  padding-bottom: 50px;
  .row {
    row-gap: 20px;
  }
}
.am-five-col {
  width: calc(100% / 5);
}
</style>
