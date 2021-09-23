<template>
  <div class="flex">
    <div class="cardList" v-for="(card, index) in getCards()" :key="index">
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
    filter: String,
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
  // computed: {
  //   filteredCardList() {
  //     let filteredList = this.cardList.filter((genere) => {
  //       if (cardList.genre == genere) {
  //         return true;
  //       }
  //       return false;
  //     });
  //     return filteredList;
  //   },
  // },
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
    getCards() {
      if (!this.filter) {
        return this.cardList;
      }
      let filteredList = this.cardList.filter((card) => {
        if (card.genre == this.filter) {
          return true;
        }
        return false;
      });
      return filteredList;
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
