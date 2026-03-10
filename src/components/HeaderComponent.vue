<script setup>
import { useDispesa } from '../composable/UseDispesa.js'

const {filter} = useDispesa()

</script>

<template>
    <div class="header">
            <h1>Controle de Gastos Rapido</h1>
            <div>
                <button class="small-btn" @click="filter = 'all'">
                <span class="mdi mdi-package-variant"></span>Tudo
                </button>

                <button class="small-btn" @click="filter = 'food'">
                <span class="mdi mdi-food"></span> Comida
                </button>

                <button class="small-btn" @click="filter = 'transport'">
                <span class="mdi mdi-train-car"></span>Transporte
                </button>

                <button class="small-btn" @click="filter = 'other'">
                <span class="mdi mdi-format-list-bulleted"></span>Outros
                </button>
            </div>
        </div>
</template>