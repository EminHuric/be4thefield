<template>
    <div class="border">
        <img src="/logo-black.jpeg" alt="logo" class="logo">

        <nav class="menu">
            <a href="#">Početna</a>
            <a href="#">O nama</a>
            <a href="#">Proizvodi</a>
            <a href="#">Kontakt</a>
        </nav>
        <p class="cart"><i class="fa-solid fa-cart-shopping"></i></p>
        <div class="hamburger" @click="toggleMenu">
            <p class="e">
            <i class="fa-solid fa-bars"></i>
            </p>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
}

</script>

<style scoped>
.e {
    color: white;
    display: none
}
.border {
    border: 1px solid rgb(29, 28, 28);
    height: 180px;
    width: 100%;
    position: fixed;
    background-color: black;
    top: 0;
    right: 0;
    z-index: 99;
}
.logo {
    height: 180px;
    margin: 0 20%;
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
@media (max-width: 759px) {
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
}
</style>