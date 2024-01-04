<template>
  <div class="products">
    <h1>Our Products</h1>
    <div class="cards">
      <div class="card" v-for="p in 6" :key="p">
        <img src="../assets/logo.svg" alt="product name" />
        <div class="card_body">
          <h6 class="card_title">Product Name {{ p }}</h6>
          <p class="card_text">Lorem ipsum dolor sit amet.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.products {
  display: flex;
  flex-direction: column;
}

h1 {
  margin: auto 15px;
}
.cards {
  display: flex;
  margin-top: 25px;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: space-around;
}
.card {
  flex-basis: 300px;
  background-color: #333;
  padding: 3px;
  border-radius: 8px;
}

.card img {
  width: 100%;
  height: 210px;
  object-fit: cover;
  border-radius: 8px 8px 0 0;
}

.card_body {
  padding: 15px 20px 20px;
}

.card_title {
  font-size: 20px;
  font-weight: 500;
  color: #fff;
}
.card_text {
  font-size: 18px;
  color: #fff;
}
</style>