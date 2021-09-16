<template>
    <div class="input-group">
        <entrada-dados @salvar="adicionarTarefa" v-model="novaTarefa" />
        <span class="input-group-btn">
        <button @click="adicionarTarefa" class="btn btn-primary">
            Adicionar tarefa
        </button>
        </span>
    </div>
</template>

<script>
import entradaDados from "@/components/templates/entradaDados"
export default {
    components: { entradaDados },
    data() {
        return {
            novaTarefa: "",
        }
    },
    methods: {
        adicionarTarefa() {
            this.$emit("adicionarTarefa", this.novaTarefa);
            this.novaTarefa = "";
        }
    }
}
</script>

<style>

</style>