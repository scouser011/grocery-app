<template>
  <div class="container">
    <div class="intro">
      <div class="heading">
        <router-link to="/stores"><img src="../assets/left.png" alt=""></router-link>
        <p>My Orders</p>
      </div>
      <img src="../assets/rice.png" alt="">
      <h2>Publix</h2>
      <p>Delivery today at 2pm <span><img src="../assets/compose.png" alt=""></span> </p>
      <div class="veggies-wrapper">
        <div v-for="(veggie, id) in veggies" :key="id">
          <Product :veggie="veggie" />
        </div>
      </div>
      <div class="delivery-fee">
        <p>Delivery fee</p>
        <p>$20</p>
      </div>
      <div class="total">
        <h3>Total</h3>
        <h4>$62.00</h4>
      </div>
      <div class="barcode">
        <img src="../assets/barcode.png" alt="">
      </div>
      <div class="button">
        <a href=""><span><img src="../assets/thumbs-up.png" alt=""></span>Checkout</a>
      </div>
    </div>
  </div>
</template>
<script>
import Product from '@/components/Product.vue'
export default {
  components: {
    Product
  },
  data () {
    return {
      veggies: [
        {
          name: 'Cucumber',
          price: '$20',
          weight: '01lb'
        },
        {
          name: 'Firm tomatoes',
          price: '$12',
          weight: '03lb'
        },
        {
          name: 'Banana',
          price: '$10',
          weight: 20
        }
      ]
    }
  }
}
</script>
<style scoped>
  .intro {
    padding-top: 50px;
  }
  .intro p {
    color: #aeb1be;
  }
  .intro p span img {
    height: 20px;
    margin: 0 0 -5px 5px}
  .intro img {
      height: 50px;
  }
  .heading {
    display: flex;
    margin-bottom: 20px;
  }
  .heading img {
    height: 30px;
  }
  .heading p {
    margin: auto 230px auto auto;
  }
  .delivery-fee {
    display: flex;
    justify-content: space-between;
    padding-bottom: 15px;
    border-bottom: dashed 2px darkgrey;
  }
  .total {
    display: flex;
    justify-content: space-between;
  }
  .barcode img {
    height: 100px;
  }
  .button {
    flex-direction: row;
    align-items: center;
    margin: auto;
    justify-content: center;
    gap: 15px;
  }
  .button img {
    width: 50px;
  }
  .button a {
    background-color: #655db0;
    color: white;
    text-decoration: none;
    width: 100%;
    border-radius: 15px;
    padding: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    margin-top: 30px;
  }
  .button a span img {
    width: 30px;
    height: 30px;
  }
</style>