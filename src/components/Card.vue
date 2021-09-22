<template>
  <div class="card">
    <img class="img-fluid mb-3" :src="info.poster" alt="" />
    <h4>{{ info.title }}</h4>
    <div>{{ info.author }}</div>
    <div class="fw-bold">{{ info.year }}</div>
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
h1 {
  font-weight: 700;
}
h4 {
  text-transform: capitalize;
}
img {
  border-radius: 50%;
  box-shadow: 0 0 6px 3px rgba(#000, 0.15);
}
</style>
