<template>
  <div class="veggie">
    <div>
      <img src="../assets/cucumber.png" alt="">
    </div>
    <div>
      <h4> {{ veggie.name }} </h4>
      <p>Instriction</p>
    </div>
    <div>
      <p> {{ veggie.price }} </p>
    </div>
    <div class="weight-and-bin">
      <p> {{ veggie.weight }} </p>
      <img src="../assets/bin.png" alt="">
    </div>
  </div>
</template>
<script>
export default {
    props: ["veggie"]
}
</script>
<style scoped>
  .veggie {
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 15px;
  }
  .weight-and-bin {
    display: flex;
    gap: 15px;
    align-items: center;
  }
  img {
    height: 30px;
  }
</style>