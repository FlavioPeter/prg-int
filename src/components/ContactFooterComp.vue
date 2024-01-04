<template>
  <div class="footer">
    <ul class="contacts">
      <li><i class="fa-solid fa-phone"></i>Phone: +1 (555) 555-5555</li>
      <li><i class="fa-solid fa-envelope"></i>Email: info@company.com</li>
    </ul>
  </div>
</template>

<script setup>
</script>

<style scoped>
ul {
  list-style: none;
}

.footer {
  position: absolute;
  width: 100%;
  bottom: 0px;
  background: #3474e6;
  color: #fff;
  height: 60px;
}

.footer ul {
  display: flex;
  justify-content: center;
}

.footer ul li {
  margin-left: 20px;
  font-weight: bold;
  padding: 15px 20px;
  min-width: 290px;
  max-height: 56px;
  color: black;
}

i {
  padding: 5px;
  color: #fff;
}
</style>