<template>
  <div class="main">
    <CardList />
  </div>
</template>

<script>
import CardList from "@/components/CardList.vue";
export default {
  name: "Main",
  props: {
    msg: String,
  },
  components: {
    CardList,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/mixins";
@import "@/style/mixins.scss";
.main {
  @include align-center();
  height: 90vh;
  width: 100%;
  background-color: #1e2d3b;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
