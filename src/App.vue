<template>
  <section>
    <cabecalho :valor="titulo"/>
    <div class="container">
      <adicionar-tarefa @adicionarTarefa="adicionarTarefa" />
      <listar-tarefas :tarefas="tarefas"/>
      <footer>
        <em>Altere aqui o titulo da sua lista de tarefas</em>
        <entrada-dados v-model="titulo" type="text" />
      </footer>
    </div>
    <rodape />
  </section>
</template>

<script>
import cabecalho from "@/components/cabecalho";
import rodape from "@/components/rodape";
import listarTarefas from "@/components/listarTarefas";
import adicionarTarefa from "@/components/adicionarTarefa";
import entradaDados from "@/components/templates/entradaDados";
export default {
  name: 'App',
  components: { 
    cabecalho, 
    rodape, 
    listarTarefas, 
    adicionarTarefa, 
    entradaDados 
  },
  data() {
    return {
      titulo: "Minha lista de tarefas",
      tarefas: [
        { titulo: "Estudar", checked: false },
        { titulo: "Programar", checked: true },
      ],
    }
  },
  methods: {
    adicionarTarefa(novaTarefa) {
      this.tarefas.push({
        titulo: novaTarefa,
        checked: false,
      });
    }
  }
}
</script>

<style>
.container {
  width: 42%;
  padding-top: 50px;
  margin: 20px auto 0px;
}

ul li {
  list-style: none;
}

.removed {
  color: gray;
}

.removed label {
  text-decoration: line-through;
}
</style>
