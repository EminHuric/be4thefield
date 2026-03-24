<template>
    <div class="intro">
        <h1 class="s">Dobro došli na zvanični sajt učeničke kompanije Be4TheField</h1>
        <p class="p">Mi smo kompanija koja se bavi proizvodnjom društvenih igara namenjenih lakšem
            i kreativnijem učenju. Kroz inovativne ideje i interaktivan pristup, trudimo
            se da unapredimo proces obrazovanja i učinimo ga zanimljivijim, efikasnijim
            i pristupačnijim kako učenicima, tako i profesorima.</p>

        <div class="container">
            <button class="btn1">O nama</button>
            <button class="btn2">Proizvodi</button>
        </div>
        <img src="/logo-black.jpeg" alt="lgo" class="logo">
    </div>
</template>
<style scoped>
.logo {
    position: absolute;
    right: 20%;
    margin-top: -540px;
    height: 720px;
}

.container {
    display: flex;
}

.intro {
    border: 1px solid black;
    height: 100vh;
    position: static;
    width: 120%;
    background-color: black;
    margin-left: -5%;
}

.s {
    color: #ffffff;
    font-size: 50px;
    margin-top: 320px;
    font-family: Arial, Helvetica, sans-serif;
    margin-left: 22%;
    width: 25%;

}

.p {
    color: rgb(200, 200, 200);
    margin-left: 22%;
    font-size: 20px;
    width: 20%;
    font-family: Arial, Helvetica, sans-serif;
}

.btn1 {
    margin-left: 22%;
    height: 50px;
    width: 150px;
    background-color: #ffffff;
    border: none;
    font-weight: bold;
    font-size: 18px;
    border-radius: 5px;
    margin-top: 20px;
}

.btn2 {
    height: 50px;
    width: 150px;
    background-color: #000000;
    border-color: white;
    font-weight: bold;
    font-size: 18px;
    border-radius: 5px;
    color: white;
    margin-left: 50px;
    margin-top: 20px;
}

@media (max-width: 1024px) {
    .intro {
        width: 108%;
        height: 10%;
        
    }

    .s {
        text-align: center;
        width: 90%;
        margin: 250px auto;
        font-size: 40px;
    }

    .p {
        text-align: center;
        font-size: 18px;
        width: 90%;
        margin: -230px auto;
    }

    .logo {
        margin-top: 500px;
    }

    .btn1 {
        margin: 250px auto;
    }

    .btn2 {
        margin: 250px auto;
    }

    .logo {
        display: none;
    }
}

@media (min-width: 1025px) and (max-width: 1500px) {
    .s {
        margin-left: 10%;
        width: 40%;
    }
    .logo {
        height: 350px;
        right: 5%;
        margin-top: -500px;
    }
    .p {
        margin-left: 10%;
        width: 35%;
    }
}
@media (min-width: 1501px) and (max-width: 1700px) {
    .s {
        margin-left: 16%;
        width: 32%;
    }
    .logo {
        height: 400px;
        right: 15%;
        margin-top: -500px;
    }
    .p {
        margin-left: 16%;
        width: 32%;
    }
    .btn1 {
        margin-left: 16%;
    }
}
@media (min-width: 1701px) and (max-width: 2500px) {
    .s {
        margin-left: 16%;
        width: 32%;
    }
    .logo {
        height: 400px;
        right: 15%;
        margin-top: -500px;
    }
    .p {
        margin-left: 16%;
        width: 32%;
    }
    .btn1 {
        margin-left: 16%;
    }
}
</style>