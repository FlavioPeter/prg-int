<template>
  <section class="boxes">
    <div class="container">
      <div class="box">
        <h2><i class="fa-solid fa-wand-magic-sparkles"></i> Magic Solution</h2>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vero, autem.
        </p>
      </div>
      <div class="box">
        <h2><i class="fa-solid fa-droplet-slash"></i> Save Water</h2>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vero, autem.
        </p>
      </div>
      <div class="box">
        <h2><i class="fas fa-arrows-alt-v"></i> Running Water</h2>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vero, autem.
        </p>
      </div>
    </div>
  </section>
</template>
  
<script setup>
</script>
  
  <style scoped>
.boxes .container {
  display: flex;
  justify-content: space-between;
}

.box {
  flex: 1;
  background: #0a51cc;
  color: #fff;
  border-radius: 10px;
  margin: 20px 10px;
  box-shadow: 0 3px 5px rgba(0, 0, 0, 0.6);
  padding: 15px 20px;
}

.box i {
  margin-right: 10px;
}

@media (max-width: 768px) {
  .boxes .container {
    display: block;
  }
}
</style>
  