<template>
  <section class="reviews-section">
    <div class="container">
      <h2 class="subtitle">Naše igre u akciji</h2>
      <h1 class="title">Reakcije učenika i profesora</h1>

      <!-- SLIDER -->
      <div class="slider">
        <div class="slider-track">
          <!-- dupliramo komentare da ide u krug -->
          <div class="comment-card" v-for="(comment, index) in doubledComments" :key="index">
            <p class="comment-text">"{{ comment.text }}"</p>
            <p class="comment-author">– {{ comment.author }}</p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
// 10+ komentara
const comments = [
  { text: 'Bilo je interesantno, dolazite češće.', author: 'Učenik 8. razreda' },
  { text: 'Deca su došla presrećna kući i odmah smo naručili 2 kompleta.', author: 'Roditelj' },
  { text: 'Igra je bila jako zanimljiva.', author: 'Učenik 7. razreda' },
  { text: 'Svi su bili jako divni.', author: 'Učenik 7. razreda' },
  { text: 'Puno je efikasnije i lakše raditi uz ovu igru.', author: 'Nastavnik' },
  { text: 'Igra mi se svidela i baš je korisna.', author: 'Učenik 8. razreda' },
  { text: 'Divni ste i baš je zanimljivo.', author: 'Učenik 7. razreda' },
  { text: 'Lepa ideja i sve pohvale.', author: 'Učenik 7. razreda' },
  { text: 'Igra je veoma kreativna i podstiče razmišljanje.', author: 'Učenik 8. razreda' },
  
]

// dupliramo niz za infinite efekat
const doubledComments = [...comments, ...comments]
</script>

<style scoped>
.reviews-section {
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
}

.title {
  font-size: clamp(28px, 5vw, 40px);
  margin-bottom: 40px;
  font-weight: 700;
}

/* SLIDER */
.slider {
  overflow: hidden;
  width: 100%;
}

.slider-track {
  display: flex;
  width: max-content;
  animation: scroll 25s linear infinite;
}

/* KARTICE */
.comment-card {
  background: #111;
  color: white;
  padding: 20px;
  margin-right: 20px;
  border-radius: 12px;
  min-width: 250px;
  max-width: 250px;
  flex-shrink: 0;
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

.comment-text {
  font-size: 14px;
  margin-bottom: 10px;
}

.comment-author {
  font-size: 12px;
  text-align: right;
  font-weight: 600;
}

/* ANIMACIJA */
@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .comment-card {
    min-width: 200px;
  }
}
</style>