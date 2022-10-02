<template>
  <div class="songs">
    <div class="song-img">
      <img class="w-100" :src="info.poster" :alt="info.title" />
    </div>

    <div class="song-info">
      <h1 class="title">{{ info.title }}</h1>
      <p class="author">{{ info.author }}</p>
      <p class="year">{{ info.year }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "SongComponent",
  props: {
    info: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/colors.scss";
.songs {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 15px;
  background-color: $bg-header;
  color: $txt-title;
  height: 100%;

  .song-img {
    margin-bottom: 20px;

    img {
      width: 200px;
      height: 200px;
      object-fit: cover;
    }
  }

  .song-info {
    margin-top: 20px;
    text-align: center;

    .title {
      color: $txt-title;
      text-transform: uppercase;
      font-size: 1.2rem;
    }

    .year,
    .author {
      color: $txt-author;
      line-height: 0.5;
      margin-top: 15px;
    }
  }
}
</style>
