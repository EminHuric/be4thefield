<template>
  <section class="contact-section">
    <div class="container">
      <h2 class="subtitle">Kontakt</h2>
      <h1 class="title">Pošaljite nam poruku</h1>

      <form 
        action="https://formsubmit.co/be4thefield@gmail.com"
        method="POST"
        class="contact-form"
      >
        <!-- Formsubmit hidden field za redirect -->
        <input type="hidden" name="_next" value="https://be4thefield.vercel.app">
        <input type="hidden" name="_captcha" value="false">

        <input type="text" name="name" placeholder="Vaše ime" required>
        <input type="email" name="email" placeholder="Vaš email" required>
        <input type="tel" name="phone" placeholder="Broj telefona">
        <textarea name="message" placeholder="Vaša poruka" required></textarea>
        <button type="submit">Pošalji</button>
      </form>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  padding: 80px 20px;
  background: #f9f9f9;
  text-align: center;
  color: #111;
}

.subtitle {
  font-size: 14px;
  color: #777;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 10px;
}

.title {
  font-size: clamp(28px, 5vw, 40px);
  margin-bottom: 40px;
  font-weight: 700;
}

.contact-form {
  display: flex;
  flex-direction: column;
  max-width: 500px;
  margin: 0 auto;
  gap: 15px;
}

.contact-form input,
.contact-form textarea {
  padding: 12px 15px;
  border-radius: 8px;
  border: 1px solid #ccc;
  font-size: 16px;
  width: 90%;
}

.contact-form textarea {
  resize: vertical;
  min-height: 120px;
}

.contact-form button {
  padding: 12px 20px;
  border: none;
  border-radius: 8px;
  background: #111;
  color: #fff;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
}

.contact-form button:hover {
  background: #333;
}
</style>