<template>
    <div id="donates-and-gifts" class="container-merry-christmas columns container-padding">
        <div class="column has-text-centered is-align-self-center">
            <img class="image-size" src="../assets/img/imgDonatesAndGifts/noelGifts.png" alt="black baby opening gift">
        </div>
        <div class="column has-text-centered is-align-self-center">
            <h1 class="title is-1 title-font title-color">Doações & Presentes</h1>
            <p class="title is-4 text-justify text-font text-color">A Associação é o resultado da união de
                pessoas, empresas e poder público que escolheram fazer a
                diferença no cenário da oncologia pediátrica. Você pode ajudar a dar continuidade a esta história de
                amor e esperança.
            </p>
            <b-button class="button is-success">Doe aqui</b-button>
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
    background-color: #7dd48b;
}

.title-color {
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
