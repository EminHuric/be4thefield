<template>
  <section class="about" id="onama">
    <div class="container">

      <h2 class="subtitle">Naš nastanak</h2>
      <h1 class="title">O nama</h1>

      <p class="text">
        Mi smo tim od 6 članova sa jasnim ciljem i snažnom vizijom da unapredimo dosadno i zastarelo obrazovanje i pokrenemo promene u celokupnom obrazovnom sistemu. Verujemo da učenje može i treba da bude zanimljivo, dinamično i inspirativno. Kroz proizvodnju edukativnih društvenih igara omogućavamo lakše usvajanje znanja i pretvaramo učenje u iskustvo koje se pamti.
      </p>

    </div>
  </section>
</template>

<style scoped>
.about {
  padding: 80px 20px;
  background: #ffffff;
  color: #111;
  margin-top: 50px;
}

.container {
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
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
  margin-bottom: 20px;
  font-weight: 700;
}

.text {
  font-size: clamp(15px, 2.5vw, 18px);
  line-height: 1.8;
  color: #444;
}

/* mobilni spacing */
@media (max-width: 480px) {
  .about {
    padding: 60px 15px;
  }
}
</style>