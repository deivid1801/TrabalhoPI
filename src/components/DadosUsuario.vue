<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  email: String,
  nome: String,
  dataN: String,
  endereco: String,
  cidade: String,
  estado: String,
  hobbies: String,
  linguagens: String,
  biografia: String,
  senha: String,
  confirmacao: String,
  mostrar: Boolean
})
</script>
<template>
  <div v-if="mostrar" class="dados-container">
    <h2>Dados do Usuário</h2>
    <ul class="dados-list">
      <li><strong>Email:</strong> {{ email }}</li>
      <li><strong>Nome:</strong> {{ nome }}</li>
      <li><strong>Data de Nascimento:</strong> {{ dataN }}</li>
      <li><strong>Endereço:</strong> {{ endereco }}</li>
      <li><strong>Cidade:</strong> {{ cidade }}</li>
      <li><strong>Estado:</strong> {{ estado }}</li>
      <li><strong>Hobbies:</strong> {{ hobbies }}</li>
      <li><strong>Linguagens de Programação:</strong> {{ linguagens }}</li>
      <li><strong>Biografia:</strong> {{ biografia }}</li>
      <li><strong>Senha:</strong> {{ senha }}</li>
      <li><strong>Confirmação de Senha:</strong> {{ confirmacao }}</li>
    </ul>
  </div>
</template>



<style scoped>
.dados-container {
  width: 80%;
  max-width: 800px;
  margin: auto;
  padding: 20px;
  background-color: #f8f9fa;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.dados-list {
  list-style-type: none;
  padding: 0;
}

.dados-list li {
  margin-bottom: 10px;
  font-size: 18px;
}

.dados-list strong {
  color: #007bff;
}
</style>
