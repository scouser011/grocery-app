<template>
    <div class="discount-wrapper">
        <div class="discount-image">
            <img src="../assets/groceries-woman.jpg" alt="">
        </div>
        <div class="discount-text">
            <p class="first"> {{ discount.name }} </p>
            <p class="second"> {{ discount.number }} </p>
        </div>
    </div>
</template>
<script>
export default {
    props: ["discount"]
}
</script>
<style scoped>
    img {
        height: 300px;
        border-radius: 50%;
    }
    .discount-wrapper {
        display: flex;
        justify-content: space-around;
        background-color: #fff3e3;
        border-radius: 25px;
    }
    .discount-image {
        margin: 20px 0;
    }
    .discount-text {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    .discount-text p {
        color: #ef8666;
        font-weight: bolder;
    }
    .second {
        font-size: 100px;
        margin: 0;
    }
</style>