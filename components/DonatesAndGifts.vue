<template>
    <div id="donates-and-gifts" class="container-merry-christmas columns container-padding">
        <div class="column has-text-centered is-align-self-center">
            <img class="image-size" src="../assets/img/imgDonatesAndGifts/noelGifts.png" alt="black baby opening gift">
        </div>
        <div class="column has-text-centered is-align-self-center">
            <h1 class="title is-1 title-font title-color">Doações & Presentes</h1>
            <p class="title is-4 text-alter text-font">A Associação é o resultado da união de
                pessoas, empresas e poder público que escolheram fazer a
                diferença no cenário da oncologia pediátrica. Você pode ajudar a dar continuidade a esta história de
                amor e esperança.
            </p>
            <b-button class="button-style"><a href="https://app.org.br/contatos/#" target="_blank">Doe aqui</a></b-button>
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
    background-color: #7dd48b;
}

.title-color {
    color: hsl(356, 75%, 45%);
}

.text-alter {
    text-align: justify;
    padding-right: 30px;
}

.button-style {
    width: 200px;
    height: 50px;
    border: #000;
    border-radius: 10px;
    font-family: 'Lobster';

}
a:link{
text-decoration:none;
color:rgb(0, 0, 0);
}

a:visited{
text-decoration:none;
color:rgb(0, 0, 0);
}

a:hover{
text-decoration:none;
color:rgb(0, 0, 0);
}

a:active{
text-decoration:none;
color:rgb(0, 0, 0);
}
.button-style:hover {
    transform: scale(0.88);
}
</style>
