<script setup>
    const props = defineProps(['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
        <div class="row">
            <div class="col"> 
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" placehold="Digite aqui a descrição da tarefa" required type="text"  class="form-control">
            </div>
            <div class="col-md-2">
                <button type="submit" class="btn btn-primary">Cadastrar</button>
            </div>
            <div class="col-md-2">
                <select @change="props.trocarFiltro" class="form-control">
                    <option value="todas">todas tarefas</option>
                    <option value="pendentes">pendentes</option>
                    <option value="finalizadas">finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>