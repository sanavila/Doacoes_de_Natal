<template>
    <section>
        <MerryChristmas />
        <DonatesAndGifts />
        <ChristmasCountDown />
    </section>
</template>

<script>
import DonatesAndGifts from "../components/DonatesAndGifts.vue";
import MerryChristmas from "../components/MerryChristmas.vue";
import ChristmasCountDown from "../components/ChristmasCountDown.vue";

export default {
    components: {
    MerryChristmas,
    DonatesAndGifts,
    ChristmasCountDown
}

}
</script>   
