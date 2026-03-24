<template>
  <footer class="site-footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-column">
          <h3>Kontakt</h3>
          <p>Email: <a href="mailto:be4thefield@gmail.com">be4thefield@gmail.com</a></p>
        </div>

        <div class="footer-column">
          <h3>Newsletter</h3>
          <p>Prijavite se za naše novosti!</p>
          <form 
            action="https://formsubmit.co/be4thefield@gmail.com" 
            method="POST"
          >
            <input type="hidden" name="_next" value="https://be4thefield.vercel.app">
            <input type="hidden" name="_captcha" value="false">
            <input type="email" name="email" placeholder="Vaš email" required>
            <button type="submit">Prijavi se</button>
          </form>
        </div>
      </div>

      <div class="footer-bottom">
        <p>© 2026 Be4TheField. Sva prava zadržana.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.site-footer {
  background: #111;
  color: #fff;
  padding: 40px 20px 20px;
  font-family: sans-serif;
  position: absolute;
  width: 100%;
  left: 0;
}

.site-footer a {
  color: #fff;
  text-decoration: none;
  transition: 0.3s;
}

.site-footer a:hover {
  color: #f0a500;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}

.footer-content {
  display: flex;
  justify-content: center;
  gap: 50px;
  flex-wrap: wrap;
  margin-bottom: 30px;
}

.footer-column h3 {
  font-size: 18px;
  margin-bottom: 10px;
}

.footer-column p {
  font-size: 14px;
  margin-bottom: 10px;
}

.footer-column form {
  display: flex;
  gap: 10px;
  justify-content: center;
  flex-wrap: wrap;
}

.footer-column input[type="email"] {
  padding: 10px 12px;
  border-radius: 5px;
  border: none;
  font-size: 14px;
}

.footer-column button {
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  background: #f0a500;
  color: #111;
  cursor: pointer;
  font-weight: 600;
  transition: 0.3s;
}

.footer-column button:hover {
  background: #fff;
}

.footer-bottom {
  text-align: center;
  font-size: 14px;
  border-top: 1px solid rgba(255,255,255,0.2);
  padding-top: 15px;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    align-items: center;
  }
  .footer-column form {
    flex-direction: column;
  }
  .footer-column input[type="email"], .footer-column button {
    width: 100%;
  }
}
</style>