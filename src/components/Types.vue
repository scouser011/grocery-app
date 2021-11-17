<template>
    <div class="type-wrapper">
        <div class="type-boxes">
            <img src="../assets/gift.png" alt="">
            <p> {{ type.name }} </p>
        </div>
    </div>
</template>
<script>
export default {
  props: ["type"]
}
</script>
<style scoped>
.type-wrapper {
  display: flex;
  justify-content: center;
  margin-bottom: 50px;
}
  .type-boxes {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 15px 82px;
    /* border: solid 1px #e2e2ec; */
    border-radius: 20px;
    background-color: #ffe0b9;
    gap: 10px;
  }
  img {
    height: 30px;
  }
</style>