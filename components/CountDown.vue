<template>
    <div class="count-down is-flex is-justify-content-space-between">
        <div class="box has-text-centered">
            <p>Dias</p>
            <h3 class="is-size-1" id="days">00</h3>
        </div>

        <div class="box has-text-centered">
            <p>Horas</p>
            <h3 class="is-size-1" id="hours">00</h3>
        </div>

        <div class="box has-text-centered">
            <p>Minutos</p>
            <h3 class="is-size-1" id="minutes">00</h3>
        </div>

        <div class="box has-text-centered">
            <p>Segundos</p>
            <h3 class="is-size-1" id="seconds">00</h3>
        </div>
    </div>
</template>
<script>
import { remove } from '@vue/shared';

export default {
  name: "CountDown",
  data () {
    return {
        interation: null
    }
  },
  methods: {
    countDownFunction () {
        const christmasData = "2022-12-25";
        const countDownTime = (new Date(christmasData)).getTime() - Date.now();
        seconds.innerHTML = Math.floor((countDownTime / 1000) % 60).toString().padStart(2, "0");
        minutes.innerHTML = Math.floor((countDownTime / (1000 * 60)) % 60).toString().padStart(2, "0");
        hours.innerHTML = Math.floor((countDownTime / (1000 * 60 * 60)) % 24).toString().padStart(2, "0");
        days.innerHTML = Math.floor((countDownTime / (1000 * 60 * 60 * 24))).toString().padStart(2, "0");
    },
    interactionCountDown () {
        this.interation = setInterval(this.countDownFunction, 1000);
    }
  },
  mounted () {
    this.countDownFunction();
    this.interactionCountDown();
  },
  beforeDestroy () {
    clearInterval(this.interation);
  }
  }
</script>
<style>
@font-face {
    font-family: "digitalFont";
    src: url("./assets/fonts/digitalFont.TTF") format("truetype");
}

.count-down {
  max-width: 80%;
  margin: auto;
  padding-left: 20px;
}

.box {
  height: 100px;
  width: 100px;
  padding: 15px;
  border-radius: 0px 15px 0px 15px;
}
.box h3 {
    font-family: digitalFont;
}
</style>
