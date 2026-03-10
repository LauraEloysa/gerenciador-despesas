<script setup>
import { useDispesa } from '../composable/UseDispesa';

const {filtered, removeExpense, clearAll, total} = useDispesa()

</script>


<template>
    <div class="tabela">
    
     <h2>Lista do dia</h2>
                <table class="table">
                    <thead>
                        <tr>
                            <th>Descricao</th>
                            <th>Categoria</th>
                            <th>Valor</th>
                            <th></th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="item in filtered" :key="item.id">
                            <td>{{ item.title }}</td>
                            <td>{{ item.category }}</td>
                            <td>{{ item.value }}</td>
                            <td>
                                <button class="small-btn" @click="removeExpense(item.id)">X</button>
                            </td>
                        </tr>
                    </tbody>
                </table>

                <div class="summary">
                    Total do dia: {{ total }}
                    <button class="small-btn" @click="clearAll">Limpar tudo</button>
                </div>
    
    </div>
</template>