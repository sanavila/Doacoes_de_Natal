<template>
    <section>
        <Snow />    
        <MerryChristmas />
        <DonatesAndGifts />
        <ChristmasCountDown />
    </section>
</template>

<script>
import DonatesAndGifts from "../components/DonatesAndGifts.vue";
import MerryChristmas from "../components/MerryChristmas.vue";
import ChristmasCountDown from "../components/ChristmasCountDown.vue";
import Snow from "../components/Snow.vue";

export default {
    components: {
    MerryChristmas,
    DonatesAndGifts,
    ChristmasCountDown,
    Snow
}

}
</script>   
