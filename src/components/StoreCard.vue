<template>
  <div class="container-publix">
    <div class="publix">
      <div>
        <img src="../assets/rice.png" />
      </div>
      <div>
        <h2>{{ store.name }}</h2>
        <ul>
          <li v-for="(product, id) in store.list" :key="id"> {{ product }} </li>
        </ul>
        <p>{{ store.paragraph }}</p>
        <a :href="store.link">Visit Store</a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["store"]
}
</script>
<style scoped>
  .publix {
    display: flex;
    justify-content: space-evenly;
    background-color: #655db0;
    margin: 20px auto;
    border-radius: 25px;
    color: #cbc8e4;
    align-items: center;
    padding: 20px;
  }
  h2 {
      display: flex;
      color: white;
  }
  ul {
    display: flex;
    gap: 40px;
    justify-content: flex-start;
    padding: 0 15px;
    list-style: none;
  }
  ul li::before {
  content: "\2022";
  color: #97e4ff;
  font-weight: bold;
  display: inline-block;
  width: 1em;
  margin-left: -1.3em;
}
  a {
      color: #f0da9b;
      text-decoration: none;
      display: flex;
  }
</style>