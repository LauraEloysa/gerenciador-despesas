<template>
    <div class="app">
        <header>
            <HeaderComponent
            />
        </header>   

        <div class="layout">
            <div class="panel" v-if="visivel">
               <AdicionarComponent/>
            </div>

            <div class="panel" v-else>
               <TabelaComponent/>
            </div>
        </div>
    </div>

    <footer>
        <button class="add-dispensa" @click="mostarComponent()" v-if="!visivel">
        <span class="mdi mdi-plus"></span> Adicionar nova despesa
        </button>
        <button class="add-dispensa" @click="mostarComponent()" v-if="visivel">
        <span class="mdi mdi-arrow-left"></span> Voltar
        </button>
    </footer>
</template>

<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import AdicionarComponent from './components/AdicionarComponent.vue';
import TabelaComponent from './components/TabelaComponent.vue';

import { ref } from 'vue';

const visivel = ref(false);

function mostarComponent(){
    visivel.value = !visivel.value
}
</script>

<style>
@import './assets/css/global.css'
</style>