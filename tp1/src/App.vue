<template>
  <b-container>
    <b-row
      ><h1>{{ titulo }}</h1></b-row
    >
    <b-row>
      <div class="cards">
        <b-card v-bind:key="tarefa.id" v-for="tarefa in tarefas" class="mb-2">
          <b-card-text>
            {{ tarefa.descricao }}
          </b-card-text>
          <b-button v-if="tarefa.statusTarefa == true" href="#" variant="dark">
            Tarefa completa</b-button
          >
          <b-button v-else href="#" variant="danger"
            >Tarefa incompleta</b-button
          >
        </b-card>
      </div>
    </b-row>
  </b-container>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";
export default {
  name: "App",
  components: {},
  data() {
    return {
      titulo: "TP1 leandro barbosa pinto",
      tarefas: [
        {
          id: 1,
          descricao: "limpar o quarto",
          statusTarefa: true,
        },
        {
          id: 2,
          descricao: "lavar a louça",
          statusTarefa: false,
        },
        {
          id: 3,
          descricao: "regar as plantas",
          statusTarefa: true,
        },
      ],
    };
  },
};
</script>

<style>
.row {
  margin-top: 100px;
  justify-content: center;
}

.cards {
  display: flex;
  flex-wrap: inherit;
  justify-content: space-around;
}

.card {
  margin-left: 10px;
}
.p {
  text-align: center;
}
</style>