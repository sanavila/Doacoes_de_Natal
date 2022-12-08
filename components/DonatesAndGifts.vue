<template>
    <div id="donates-and-gifts" class="container-merry-christmas columns container-padding">
        <div class="column has-text-centered is-align-self-center">
            <img class="image-size" src="../assets/img/imgDonatesAndGifts/noelGifts.png" alt="black baby opening gift">
        </div>
        <div class="column has-text-centered is-align-self-center">
            <h1 class="title is-1 title-font title-color">Doações & Presentes</h1>
            <p class="title is-4 text-justify text-font text-color">"Somos uma instituição sem fins lucrativos, tendo nossas
                operações possíveis a partir de doações de pessoas e empresas que acreditam em nosso trabalho. Todo
                valor é importante para levarmos um lindo natal para milhares de famílias"
            </p>
            <b-button class="text-font">doe</b-button>
        </div>
    </div>
</template>

<script>
export default {
    name: "DonatesAndGifts"
}
</script>
<style>
@import "../assets/css/main.css";

#donates-and-gifts {
    max-height: 500px;
    background-color: hsl(240, 9%, 96%);
}

.title-color{
    color: hsl(356, 75%, 45%);
}

.text-justify {
    text-align: justify;
    padding-right: 25px;
}
.text-color {
    color: black;
}
</style>
