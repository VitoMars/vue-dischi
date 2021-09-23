<template>
  <div class="select">
    <select
      class="form-select"
      aria-label="Default select example"
      v-model="genere"
      @change="$emit('perform', genere)"
    >
      <option selected value="">Seleziona un genere</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Select",
  data() {
    return {
      genere: "",
    };
  },
};
</script>

<style scoped lang="scss">
.select {
  position: absolute;
  top: 25px;
  right: 50px;
  width: 200px;
}
</style>
