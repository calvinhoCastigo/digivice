<script lang="ts">

export default {
    name: "Digivice",
    props: {
        digimonArt: {
            type: String,
            default: "null"
        }
    }

};


</script>

<template>
    <div id='base'>
        <div id='borda_display'>
            <div id='circulo_interno_borda_display'>
                <div id="tela">
                    <img id="img" :src="digimonArt" alt="">
                </div>
            </div>
        </div>
        <div id="cont_botoes">
            <button></button>
            <button></button>
        </div>
    </div>
</template>

<style scoped>
#base,
#borda_display,
#circulo_interno_borda_display,
#tela {

    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

#base {
    width: 400px;
    height: 400px;
    background-color: #32a2ba;
    border-top-right-radius: 20px;
    border-bottom-left-radius: 20px;
    border-bottom-right-radius: 100px;
    border-top-left-radius: 150px;
    border-bottom: solid 35px #323b4a;

}

#borda_display {
    border-radius: 100%;
    width: 270px;
    height: 270px;
    background-color: #a3b1c7;
    border-style: solid;
    border-color: #9aa4b5;
    border-width: 2px;
    box-shadow: 0px 7px 5px #565558;
    transform:
}

#circulo_interno_borda_display {
    border-radius: 100%;
    width: 200px;
    height: 200px;
    background-color: #323b4a;
}

#tela {
    background-color: #a3b1c7;
    width: 130px;
    height: 130px;
    overflow: hidden;
    border-radius: 5px;
}

#tela img {
    height: 100%;
    filter: hue-rotate(90deg);
}

#cont_botoes {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: row;
    width: 100%;
    margin-left: 50px;
}

#cont_botoes button {
    background-color: #daf23d;
    border-radius: 100%;
    height: 50px;
    width: 50px;
    border: none;
    margin-left: 10px;
    box-shadow: 0px 7px 5px #565558;
    border-bottom: solid 4px #93a32a;
    cursor: pointer
}
</style>
