<template>
  <nav> <!-- Menu de navegação do site --></nav>
  <aside><!-- Conteúdo secundário/lateral do site --></aside>
  <main>
    <!-- Conteúdo principal do site -->
    <h1>CONTADOR</h1>
    <h4>Instituto Evoluir</h4>
    <!-- 03. Utilizar o componente -->
    <MadCounter />
    <Message>{{ message }}</Message>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

// 01. Importar o arquivo do componente
import MadCounter from '@/components/MadCounter.vue'
import Message from '@/components/Message.vue'

export default defineComponent({
  name: 'MainView',
  props: {
    message: String,
    title: String
  },
  // 02. Listar os componentes que serão utilizados
  components: {
    Message,
    MadCounter
  },
});
</script>

<style scoped>
* {
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
h1, h4 {
  display: flex;
  justify-content: center;
}
</style>