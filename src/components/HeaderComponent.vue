<template>
  <header>
    <img src="../assets/img/Spotify_icon.svg.png" alt="Spotify" />
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/colors.scss";
header {
  background-color: $bg-header;
  height: 50px;
  padding: 10px;
  img {
    height: 30px;
  }
}
</style>
