<template>
  <div class="carta">
    <img class="img-fluid mb-3" :src="info.poster" alt="" />
    <h5>{{ info.title }}</h5>
    <div class="little-text">{{ info.author }}</div>
    <div class="little-text">{{ info.year }}</div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["info"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.carta {
  display: flex;
  flex-direction: column;
  align-items: center;
  //   height: 200px;
  //   width: 200px;
  padding: 20px;
  background-color: #2e3a46;

  img {
    height: 100px;
  }
  h5 {
    color: white;
    text-transform: uppercase;
  }
  .little-text {
    color: grey;
  }
}
</style>
