<script setup>
    const props = defineProps(['adicionaTarefa', 'tarefaTemp', 'getTarefasFiltradas', 'editaTarefaTemp'])
</script>

<template>
    <form @submit.prevent="props.adicionaTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.tarefaTemp" @change="props.editaTarefaTemp" required
                    type="text" placeholder="Digite a descição da tarefa" class="form-control">
            </div>
            <div class="col-md-1">
                <button type="submit" class="btn btn-primary">Adicionar</button>
            </div>
            <div class="col-md-2">
                <select @change="props.getTarefasFiltradas" class="form-control">
                    <option value="todas">Todas as tarefas</option>
                    <option value="pendentes">Tarefas pendentes</option>
                    <option value="finalizadas">Tarefas finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>