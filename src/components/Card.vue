<template>
  <div class="carta">
    <img class="img-fluid mb-3" :src="info.poster" alt="" />
    <div class="title">{{ info.title }}</div>
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
  height: 300px;
  width: 200px;
  margin: 20px;
  padding: 20px;
  background-color: #2e3a46;

  img {
    height: 100px;
  }
  .title {
    font-size: 18px;
    padding-bottom: 20px;
    color: white;
    text-transform: uppercase;
    text-align: center;
  }
  .little-text {
    text-align: center;
    color: grey;
  }
}
</style>
