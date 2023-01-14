<script setup>
import { ref, onMounted } from 'vue'

const animClass = ref('wtf')

onMounted(() => {
    setTimeout(function () {
        animClass.value = "hide";
        console.log("WELCOME: Carolingian Royalty Registery")
    }, 5000);
})

</script>

<template>
<img alt="Vue logo" class="responsive" src="./assets/kai.svg" height="100%" />

<div :class="animClass">
        <div>
            <div class="logo_container">
                <img class="logo" alt="flag"  src="./assets/NPPA_logo.svg" />
                <p class="logo center">
                    LOADING..
                </p>
            </div>
            
        </div>
    </div>

</template>


<style scoped>
*{
    background-color: #EDD7A7;
}
.responsive{
height:100vh;
width:100vw;
}
.center{
    text-align: center;
}
.logo{
    background: rgb(21, 10, 10);
}

.wtf {
    width: 100%;
    height: 100vh;
    top: 0;
    left: 0;
    position: fixed;
    display: flex;
}

.wtf div {
    width: 100%;
    height: 100%;
    background: rgb(21, 10, 10);
    animation: up 5s ease-in forwards;
    transform: scaleY(0);
    /* background: rgb(211, 34, 3); */
}

@keyframes up {

    100% {
        transform-origin: top;
        /* transform: scaleY(0);*/
        transform: translateY(100%);
    }

    0% {
        transform-origin: bottom;
        /* transform: scaleY(1); */
        transform: translateY(-0%);
    }
}

.hide {
    visibility: hidden;
}
</style>