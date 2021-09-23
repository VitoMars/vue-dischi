<template>
  <div class="select">
    <select class="form-select" aria-label="Default select example">
      <option selected value="null">Seleziona un genere</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.select {
  position: absolute;
  top: 25px;
  right: 50px;
  width: 200px;
}
</style>
