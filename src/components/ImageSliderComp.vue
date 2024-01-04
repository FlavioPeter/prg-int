<template>
  <div class="container">
    <div class="slider">
      <div class="slides">
        <input
          v-for="n in 4"
          :key="n"
          type="radio"
          :id="'radio' + n"
          name="radio-btn"
          v-model="counter"
          :value="n"
          @click="counter = n"
        />

        <div class="slide first">
          <img src="../assets/logo.svg" alt="my img 1" />
        </div>
        <div class="slide"><img src="../assets/logo.svg" alt="my img 2" /></div>
        <div class="slide"><img src="../assets/logo.svg" alt="my img 3" /></div>
        <div class="slide"><img src="../assets/logo.svg" alt="my img 4" /></div>
      </div>

      <div class="navigation-manual">
        <label
          v-for="n in 4"
          :key="n"
          :for="'radio' + n"
          class="manual-btn"
          :style="{ background: counter == n ? 'blue' : 'white' }"
        ></label>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

var counter = ref(1);

setInterval(() => {
  counter.value++;
  if (counter.value > 4) {
    counter.value = 1;
  }
}, 5000);
</script>

<style scoped>
.container {
  padding-bottom: 10px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  border-top: solid 20px seagreen;
  border-bottom: solid 20px seagreen;
  border-radius: 20px;
}
.slider {
  width: 800px;
  height: 500px;
  border-radius: 10px;
  overflow: hidden;
}

.slides {
  width: 500%;
  height: 500px;
  display: flex;
}

.slides input {
  display: none;
}

.slide {
  width: 20%;
  transition: 2s;
}

.slide img {
  width: 800px;
  height: 500px;
}

.navigation-manual {
  position: absolute;
  width: 800px;
  margin-top: -40px;
  display: flex;
  justify-content: center;
}

.manual-btn {
  border: 2px solid #40d3dc;
  padding: 5px;
  border-radius: 10px;
  cursor: pointer;
  transition: 1s;
}

.manual-btn:not(:last-child) {
  margin-right: 40px;
}

.manual-btn:hover {
  background: #40d3dc;
}

#radio1:checked ~ .first {
  margin-left: 0%;
}

#radio2:checked ~ .first {
  margin-left: -20%;
}

#radio3:checked ~ .first {
  margin-left: -40%;
}

#radio4:checked ~ .first {
  margin-left: -60%;
}
</style>