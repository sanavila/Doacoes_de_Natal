<template>
    <div id="merry-christmas" class="container-merry-christmas columns container-padding">
        <div class="column  has-text-centered is-align-self-center">
            <h1 class="title is-1 title-font title-two-containers">Feliz Natal!</h1>
            <p class="title is-4 text-font color-two-containers">O verdadeiro espírito do Natal encontra-se presente em
                todas as boas ações
                que fazemos durante a nossa vida.</p>
            <audio controls :src="music">
                Seu navegador não suporta esse audio
            </audio>
        </div>
        <div class="column has-text-centered is-align-self-center">
            <img class="image-size" src="../assets/img/imgMerryChristmas/papai-noel.png"
                alt="santa claus, a snowman and a reindeer smiling">
        </div>
    </div>
</template>

<script>
import music from "@/static/audios/jinglebell.mp3";

export default {
    name: "MerryChristmas",
    data() {
        return {
            music
        }
    }
}
</script>
<style>
@import "../assets/css/main.css";
</style>
