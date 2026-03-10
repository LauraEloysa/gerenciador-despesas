<template>
    <div class="app">
        <header>
            <HeaderComponent />
        </header>

        <div class="layout">
            <div class="panel" v-if="visivel">
                <AdicionarComponent />
            </div>

            <div class="panel" v-else>
                <TabelaComponent />
            </div>
        </div>


        <footer>
            <button class="add-principal" @click="mostarComponent()" v-if="!visivel">
                <span class="mdi mdi-plus"></span> Adicionar nova despesa
            </button>
            <button class="add-principal" @click="mostarComponent()" v-if="visivel">
                <span class="mdi mdi-arrow-left"></span> Voltar
            </button>
        </footer>
    </div>


</template>

<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import AdicionarComponent from './components/AdicionarComponent.vue';
import TabelaComponent from './components/TabelaComponent.vue';
import { useDispesa } from './composable/UseDispesa';

const { mostarComponent, visivel } = useDispesa();
</script>

<style>
@import './assets/css/global.css'
</style>