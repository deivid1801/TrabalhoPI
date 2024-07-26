<script setup>
import { ref } from 'vue'
import FormularioComponent from './components/FormularioComponent.vue'
import DadosUsuario from './components/DadosUsuario.vue'

const dados = ref({
  email: '',
  nome: '',
  dataN: '',
  endereco: '',
  cidade: '',
  estado: '',
  hobbies: '',
  linguagens: '',
  biografia: '',
  senha: '',
  confirmacao: ''
})

const mostrarDados = ref(false)

function handleMostrarDados(dadosFormulario) {
  dados.value = dadosFormulario
  mostrarDados.value = true
}

function handleDadosLimpos() {
  dados.value = {
    email: '',
    nome: '',
    dataN: '',
    endereco: '',
    cidade: '',
    estado: '',
    hobbies: '',
    linguagens: '',
    biografia: '',
    senha: '',
    confirmacao: ''
  }
  mostrarDados.value = false
}
</script>
<template>
  <div id="app">
    <h1 class="text-center">Meu Formulário de Dados</h1>
    <FormularioComponent
      @mostrarDados="handleMostrarDados"
      @dadosLimpos="handleDadosLimpos"
    />
    <DadosUsuario
      :email="dados.email"
      :nome="dados.nome"
      :dataN="dados.dataN"
      :endereco="dados.endereco"
      :cidade="dados.cidade"
      :estado="dados.estado"
      :hobbies="dados.hobbies"
      :linguagens="dados.linguagens"
      :biografia="dados.biografia"
      :senha="dados.senha"
      :confirmacao="dados.confirmacao"
      :mostrar="mostrarDados"
    />
  </div>
</template>


<style>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #e9ecef;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
h1 {
  color: #007bff;
  margin-bottom: 20px;
}
</style>
