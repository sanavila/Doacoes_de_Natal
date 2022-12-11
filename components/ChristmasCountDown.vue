<template>
  <div id="christmas-count-down" class="container-merry-christmas columns container-padding">
    <div class="column has-text-centered is-align-self-center">
      <h1 class="title is-1 title-font title-two-containers">O Natal está chegando!</h1>
      <p class="title is-4 text-font color-two-containers">Que o espírito natalino viva mais do que apenas um dia no
        ano.</p>
      <CountDown />
    </div>
    <div class="column  has-text-centered is-align-self-center">
      <img class="image-size" src="../assets/img/imgChristmasCountDown/papaiNoelsorrindo.png" alt="santa claus smiling">
    </div>
  </div>
</template>

<script>
import CountDown from "./CountDown.vue"
export default {
  name: "ChristmasCountDown",
  components: {
    CountDown
  }
}
</script>
<style>
@import "../assets/css/main.css";

</style>
