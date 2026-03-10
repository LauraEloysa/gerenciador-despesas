<script setup>
import { useDispesa } from '../composable/UseDispesa';

const { title, value, category, addExpense,} = useDispesa()
</script>

<template>
    <div>

        <h2>Nova despesa</h2>
        <input v-model="title" class="input" placeholder="Descricao" />
        <input v-model="value" class="input" placeholder="Valor" />
        <input v-model="category" class="input" placeholder="Categoria" />
        <div class="row">
            <button class="small-btn" @click="addExpense">Add</button>
            
        </div>

    </div>
</template>