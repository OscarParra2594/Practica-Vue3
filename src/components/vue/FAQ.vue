<script setup>
import { ref } from 'vue';

const showTheme1 = ref(true);
const showTheme2 = ref(false);
const showTheme3 = ref(false);
const showTheme4 = ref(false);

function showInfo(index) {     //esta funcion sirve para hacer un switch que muestre  y guarde la caja donde va el texto
    if(index == 1){
        showTheme1.value = true
        showTheme2.value = false
        showTheme3.value = false
        showTheme4.value = false
}
if(index == 2){
        showTheme1.value = false
        showTheme2.value = true
        showTheme3.value = false
        showTheme4.value = false
}
if(index == 3){
        showTheme1.value = false
        showTheme2.value = false
        showTheme3.value = true
        showTheme4.value = false
}
if(index == 4){
        showTheme1.value = false
        showTheme2.value = false
        showTheme3.value = false
        showTheme4.value = true
}
}

</script>

<template>
    <!-- texto 1 -->
    <div class="bg-blue-500 p-1 max-w-60 mt-12 mx-auto rounded text-center font-bold">

        <div class="bg-blue-400 rounded text-center font-bold">

            <h1 @click="showInfo(1)"
                class="hover:cursor-pointer bg-blue-300 text-white px-1  flex justify-between text-center">
                Tema 1 <span class="cursor-pointer font-bold">+</span>

            </h1>

            <div v-show="showTheme1" class="bg-blue-200 p-1 mt-1">Texto del tema 1
            </div>
        </div>

        <!-- texto 2 -->
        <div class="bg-blue-400 rounded text-center font-bold">

            <h1 @click="showInfo(2)"
                class="hover:cursor-pointer bg-blue-300 text-white px-1  flex justify-between text-center">
                Tema 2 <span class="cursor-pointer font-bold">+</span>

            </h1>

            <div v-show="showTheme2" class="bg-blue-200 p-1 mt-1">Texto del tema 2
            </div>
        </div>

        <!-- texto 3 -->
        <div class="bg-blue-400 rounded text-center font-bold">

            <h1 @click="showInfo(3)"
                class="hover:cursor-pointer bg-blue-300 text-white px-1  flex justify-between text-center">
                Tema 3 <span class="cursor-pointer font-bold">+</span>

            </h1>

            <div v-show="showTheme3" class="bg-blue-200 p-1 mt-1">Texto del tema 3
            </div>
        </div>
        <!-- texto 4 -->
        <div class="bg-blue-400 rounded text-center font-bold">

            <h1 @click="showInfo(4)"
                class="hover:cursor-pointer bg-blue-300 text-white px-1  flex justify-between text-center">
                Tema 4 <span class="cursor-pointer font-bold">+</span>

            </h1>

            <div v-show="showTheme4" class="bg-blue-200 p-1 mt-1">Texto del tema 4
            </div>
        </div>

    </div>
</template>