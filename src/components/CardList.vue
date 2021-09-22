<template>
  <div class="flex">
    <div
      v-for="(card, index) in cardList"
      :key="index"
      class="col-6 col-md-4 col-lg-3 my-5"
    >
      <Card :info="card" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Card from "./Card.vue";
export default {
  name: "CardList",
  props: {
    msg: String,
  },
  components: {
    Card,
  },
  data() {
    return {
      APIUrl: "https://flynn.boolean.careers/exercises/api/array/music",
      cardList: [],
    };
  },
  created() {
    this.getCard();
  },
  methods: {
    getCard() {
      axios
        .get(this.APIUrl)
        .then((res) => {
          this.cardList = res.data.response;
        })
        .catch((err) => {
          console.log("Error ", err);
        });
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/style/mixins";
.flex {
  @include center-content();
  @include center();
  flex-wrap: wrap;
}
</style>
