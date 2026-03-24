<template>
  <section class="product-section" id="product">
    <h2 class="subtitle">Proizvodi</h2>
    <h1 class="title">Naša igra</h1>

    <div class="product-content">
      <!-- SLIKA -->
      <div class="product-image-container">
        <img src="/product.jpeg" alt="Edukativna igra" class="product-image">
      </div>

      <!-- INFO -->
      <div class="product-info">
        <h3 class="product-name">CONTI MAKERS</h3>
        <p class="product-description">
            Društvena igra kreirana prvenstveno za učenike 7. i 8. razreda,
             dizajnirana da ubrza i olakša usvajanje geografskog gradiva.
              Pruža interaktivno i zabavno iskustvo za učenike i profesore,
               a istovremeno oduševljava sve ljubitelje geografije koji žele
                da učenje bude uzbudljivo i inspirativno.
        </p>
        <p class="product-price">1699.99 RSD</p>
        <button class="buy-btn">Kupi</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.product-section {
  padding: 80px 20px;
  background: #ffffff;
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
  font-size: clamp(28px, 5vw, 48px);
  margin-bottom: 40px;
  font-weight: 700;
}

.product-content {
  display: flex;
  gap: 50px;
  align-items: flex-start;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
  flex-wrap: wrap;
}

/* SLIKA */
.product-image-container {
  flex: 1;
  min-width: 300px;
  display: flex;
  justify-content: center;
}

.product-image {
  width: 100%;
  max-width: 450px;
  height: auto;
  border-radius: 15px;
  border: 2px solid #eee;
  box-shadow: 0 10px 25px rgba(0,0,0,0.1);
  object-fit: cover;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.product-image:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.2);
}

/* INFO */
.product-info {
  flex: 1;
  min-width: 300px;
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.product-name {
  font-size: 26px;
  font-weight: 700;
  margin-bottom: 15px;
}

.product-description {
  font-size: 16px;
  line-height: 1.8;
  margin-bottom: 20px;
  color: #444;
}

.product-price {
  font-size: 22px;
  font-weight: 700;
  margin-bottom: 20px;
}

.buy-btn {
  background: #111;
  color: white;
  border: none;
  padding: 14px 30px;
  font-size: 16px;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.3s ease;
  align-self: start;
}

.buy-btn:hover {
  background: #333;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .product-content {
    flex-direction: column;
    text-align: center;
  }

  .product-info {
    text-align: center;
  }

  .buy-btn {
    width: 60%;
    margin: 0 auto;
  }

  .product-image {
    max-width: 90%;
  }
}
</style>