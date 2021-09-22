<template>
  <div class="header">
    <img src="@/assets/logo.png" alt="" />
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/mixins.scss";
.header {
  @include align-center();
  height: 100px;
  width: 100%;
  padding: 0px 20px;
  background-color: #2e3a46;
  img {
    height: 70px;
  }
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
