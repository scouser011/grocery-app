<template>

  <div>
    <div class="container">
      <div class="intro">
        <p>N 200, Lake Geneva</p>
        <img src="../assets/map.png" alt="">
        <p>Choose store</p>
        <div class="type-container">
          <div v-for="(type, id) in types" :key="id">
            <Types :type="type" />
          </div>
        </div>
        <router-link to="/orders" style="text-decoration: none;">
          <div v-for="(store, id) in stores" :key="id">
            <StoreCard :store="store" />
          </div>
        </router-link>
        <div>
          <Discounts :discount="discounts"/>
        </div>
      </div>
    </div>
  </div>
  
</template>
<script>
import StoreCard from '@/components/StoreCard'
import Types from '@/components/Types'
import Discounts from '@/components/Discounts'
export default {
  components: {
    StoreCard,
    Types,
    Discounts
  },
  data() {
    return {
      stores: [
      {
        name: 'Publix',
        img: '../assets/rice.png',
        list: ["Grocery", "Product"],
        paragraph: "Fresh organic groceries at your door step",
        link: 'https://liverpoolfc.tv'
      },
      {
        name: 'Kroger',
        img: '../assets/ham.png',
        list: ["Meat", "Organic"],
        paragraph: "Delivering fresh organic meat at your home",
        link: 'https://polovniautomobili.com'
      }
    ],
      types: [
        {
          name: "Delivery"
        },
        {
          name: "Pickup"
        }
      ],
      discounts: {
        name: 'Discount upto',
        number: '50%'
      }
    }
  }
}
</script>
<style scoped>
  img {
    width: 30px;
  }
  .type-container {
    display: flex;
    justify-content: center;
    gap: 20px;
  }
  .intro {
    padding-top: 50px;
  }
  .intro p {
    color: #c5c8d1;
  }
</style>