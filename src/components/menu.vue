<template>
    <div class="border">
        <img src="/logo-black.jpeg" alt="logo" class="logo">

        <nav class="menu">
            <a href="#">Početna</a>
            <a href="#onama">O nama</a>
            <a href="#product">Proizvodi</a>
            <a href="#kontakt">Kontakt</a>
        </nav>
        <p class="cart"><i class="fa-solid fa-cart-shopping"></i></p>

        <div class="hamburger" @click="toggleMenu">
      <i v-if="!menuOpen" class="fa-solid fa-bars"></i>
      <i v-else class="fa-solid fa-xmark"></i>
    </div>

        <div v-if="menuOpen" class="overlay" @click="toggleMenu"></div>
        

        <!-- MOBILE MENU -->
    <div :class="['mobileMenu', menuOpen ? 'active' : '']">
  <a href="#" @click="toggleMenu">Početna</a>
  <a href="#onama" @click="toggleMenu">O nama</a>
  <a href="#product" @click="toggleMenu">Proizvodi</a>
  <a href="#kontakt" @click="toggleMenu">Kontakt</a>
</div> 

    </div>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}
</script>

<style scoped>
.hamburger {
  display: none;
  color: white;
  font-size: 48px;
  cursor: pointer;
  position: absolute;
  right: 5%;
  margin-top: -120px;
}
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.7);
  z-index: 98;
}
.mobileMenu {
  position: fixed;
  top: -500px;
  left: 50%;
  transform: translateX(-50%);
  width: 90%;
  background: rgb(25, 25, 25);
  border-radius: 10px;
  text-align: center;
  padding: 20px 0;
  transition: 0.3s ease;
  z-index: 99;
}
.mobileMenu a {
  display: block;
  color: white;
  text-decoration: none;
  padding: 15px 0;
  font-size: 20px;
}
.mobileMenu.active {
  top: 120px;
}
.e {
    color: white;
    display: none
}
.border {
    border: 1px solid rgb(29, 28, 28);
    height: 160px;
    width: 100%;
    position: fixed;
    background-color: black;
    top: 0;
    right: 0;
    z-index: 99;
}
.logo {
    height: 160px;
    margin: 0 20%;
    border-radius: 12px;
}
.menu {
    margin-top: -100px;
    margin-left: 30%;
}

.menu a {
    color: white;
    text-decoration: none;
    margin-left: 150px;
    font-size: 22px;
    font-weight: 500;
}
.cart {
    color: white;
    position: absolute;
    right: 20%;
    margin-top: -30px;
    font-size: 24px;
}
@media (max-width: 1024px) {
    .menu a, .cart {
        display: none;
    }
    .logo {
        margin-left: 3%;
    }
    .border {
        position: fixed;
        width: 100%;
        left: 0;
    }
    .e {
        display: block;
        position: absolute;
        right: 9%;
        font-size: 40px;
        margin-top: -10px;
    }
    .menu,
  .cart {
    display: none;
  }

  .hamburger {
    display: block;
  }
}
@media (min-width: 1025px) and (max-width: 1500px) {
    .logo {
        margin-left: 5%;
    }
    .menu {
        margin-left: 180px;
    }
    .menu a {
        margin-left: 100px;
    }
    .cart {
        position: absolute;
        right: 50px;
    }
    
}
@media (min-width: 1501px) and (max-width: 1700px) {
    .logo {
        margin-left: 12%;
    }
    .menu {
        margin-left: 320px;
    }
    .menu a {
        margin-left: 120px;
    }

}
@media (min-width: 1701px) and (max-width: 2000px) {
    .logo {
        margin-left: 12%;
    }
    .menu {
        margin-left: 320px;
    }
    .menu a {
        margin-left: 120px;
    }

}
</style>