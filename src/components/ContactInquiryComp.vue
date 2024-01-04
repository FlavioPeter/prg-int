<template>
  <div class="container">
    <form @onsubmit="sendEmail">
      <h3>Get in touch</h3>
      <input type="text" id="name" placeholder="Your name" required />
      <input type="email" id="email" placeholder="Email" required />
      <input type="text" id="phone" placeholder="Phone no." required />
      <select id="subject">
        <option value="question">Question</option>
        <option value="order">Order</option>
      </select>
      <textarea
        placeholder="How can we help?"
        name="message"
        id=""
        rows="5"
      ></textarea>
      <button type="submit">Send</button>
    </form>
  </div>
</template>

<script setup>
function sendEmail() {
  sendEmail
    .send({
      Host: "smtp.gmail.com",
      Username: "username",
      Password: "password",
      To: "them@website.com",
      From: "you@isp.com",
      Subject: "This is the subject",
      Body: "And this is the body",
    })
    .then(() => alert("sent"));
}
</script>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 90vh; /* Ensure the container takes up the full height of the viewport */
}

form {
  background: #fff;
  display: flex;
  flex-direction: column;
  padding: 2vw 4vw;
  width: 90%;
  height: 70%;
  min-height: 600px;
  max-width: 600px;
  border-radius: 10px;
}

form h3 {
  color: #555;
  font-weight: 800;
  margin-bottom: 20px;
}

form input,
form textarea {
  border: 0;
  margin: 10px 0;
  padding: 20px;
  outline: none;
  background: #f5f5f5;
  font-size: 16px;
  max-width: 100%;
  min-width: 100%;
  min-height: 75px;
}

form button,
form select {
  padding: 15px;
  font-size: 18px;
  border: 0;
  outline: none;
  cursor: pointer;
}

form button {
  background: #ff5361;
  color: #fff;
  width: 150px;
  margin: 20px auto 0;
  border-radius: 30px;
  font-weight: bold;
}
</style>