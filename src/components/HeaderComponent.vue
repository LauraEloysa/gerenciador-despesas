<script setup>
import { useDispesa } from '../composable/UseDispesa.js'

const {filter, visivel } = useDispesa()

</script>

<template>
    <div class="header">
            <h1> <span class="mdi mdi-file-document-edit"></span> Controle de Gastos Rapido</h1>
            <div class="class" v-if="!visivel">
                <button class="class-btn" @click="filter = 'all'">
                <span class="mdi mdi-package-variant"></span>Tudo
                </button>

                <button class="class-btn" @click="filter = 'food'">
                <span class="mdi mdi-food"></span> Comida
                </button>

                <button class="class-btn" @click="filter = 'transport'">
                <span class="mdi mdi-train-car"></span>Transporte
                </button>

                <button class="class-btn" @click="filter = 'other'">
                <span class="mdi mdi-format-list-bulleted"></span>Outros
                </button>
            </div>
        </div>
</template>