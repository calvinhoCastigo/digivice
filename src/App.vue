<script lang="ts">
import Digivice from "./components/Digivice.vue";

import axios from 'axios';

export default {
    name: "App",
    data() {
        return {
            digimon: this.fetchDigimon(1)
        }
    },
    methods: {
        fetchDigimon: async function (id: number) {

            const url = "https://digi-api.com/api/v1/digimon/" + id;

            const response = await axios.get(url);
            return response.data;
            console.log(this.digimon);
        }


    },
    components: { Digivice }
};


</script>

<template>
    <main>
        <Digivice :digimonArt="digimon.images[0].href" />
    </main>
    <section>

    </section>
</template>

<style scoped></style>
