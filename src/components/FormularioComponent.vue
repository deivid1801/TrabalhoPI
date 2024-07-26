<script setup>
import { ref, defineEmits } from 'vue'

const email = ref('')
const nome = ref('')
const dataN = ref('')
const endereco = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const linguagens = ref('')
const biografia = ref('')
const senha = ref('')
const confirmacao = ref('')

const emit = defineEmits(['mostrarDados', 'dadosLimpos'])

function limparDados() {
  email.value = ""
  nome.value = ""
  dataN.value = ""
  endereco.value = ""
  cidade.value = ""
  estado.value = ""
  hobbies.value = ""
  linguagens.value = ""
  biografia.value = ""
  senha.value = ""
  confirmacao.value = ""
  emit('dadosLimpos', { email: email.value, nome: nome.value, dataN: dataN.value, endereco: endereco.value, cidade: cidade.value, estado: estado.value, hobbies: hobbies.value, linguagens: linguagens.value, biografia: biografia.value, senha: senha.value, confirmacao: confirmacao.value })
}

function emitirMostrarDados() {
  emit('mostrarDados', {
    email: email.value,
    nome: nome.value,
    dataN: dataN.value,
    endereco: endereco.value,
    cidade: cidade.value,
    estado: estado.value,
    hobbies: hobbies.value,
    linguagens: linguagens.value,
    biografia: biografia.value,
    senha: senha.value,
    confirmacao: confirmacao.value
  })
}
</script>
<template>
  <div class="form-container">
    <form class="edit">
      <div class="form-group">
        <label for="email">Email:</label>
        <input id="email" type="email" v-model="email" class="form-control" placeholder="Enter email">
      </div>
      <div class="form-group">
        <label for="nome">Nome:</label>
        <input id="nome" type="text" v-model="nome" class="form-control" placeholder="Insira seu nome">
      </div>
      <div class="form-group">
        <label for="dataN">Data de Nascimento:</label>
        <input id="dataN" type="date" v-model="dataN" class="form-control">
      </div>
      <div class="form-group">
        <label for="endereco">Endereço:</label>
        <input id="endereco" type="text" v-model="endereco" class="form-control" placeholder="Insira seu endereço">
      </div>
      <div class="form-group">
        <label for="cidade">Cidade:</label>
        <input id="cidade" type="text" v-model="cidade" class="form-control" placeholder="Insira sua cidade">
      </div>
      <div class="form-group">
        <label for="estado">Estado:</label>
        <select id="estado" v-model="estado" class="form-select">
          <option value="" disabled>Selecione seu estado</option>
          <!-- Lista de estados -->
          <option>AC</option>
          <option>AL</option>
          <option>AM</option>
          <option>BA</option>
          <option>CE</option>
          <option>DF</option>
          <option>ES</option>
          <option>GO</option>
          <option>MA</option>
          <option>MG</option>
          <option>MS</option>
          <option>MT</option>
          <option>PA</option>
          <option>PB</option>
          <option>PE</option>
          <option>PI</option>
          <option>PR</option>
          <option>RJ</option>
          <option>RN</option>
          <option>RO</option>
          <option>RR</option>
          <option>RS</option>
          <option>SC</option>
          <option>SE</option>
          <option>SP</option>
          <option>TO</option>
        </select>
      </div>
      <div class="form-group">
        <label for="hobbies">Hobbies:</label>
        <input id="hobbies" type="text" v-model="hobbies" class="form-control" placeholder="Insira seus hobbies">
      </div>
      <div class="form-group">
        <label for="linguagens">Linguagens de Programação:</label>
        <input id="linguagens" type="text" v-model="linguagens" class="form-control" placeholder="Insira suas linguagens de programação">
      </div>
      <div class="form-group">
        <label for="biografia">Biografia:</label>
        <textarea id="biografia" v-model="biografia" class="form-control" rows="3" placeholder="Insira sua biografia"></textarea>
      </div>
      <div class="form-group">
        <label for="senha">Senha:</label>
        <input id="senha" type="password" v-model="senha" class="form-control" placeholder="Insira sua senha">
      </div>
      <div class="form-group">
        <label for="confirmacao">Confirmação de Senha:</label>
        <input id="confirmacao" type="password" v-model="confirmacao" class="form-control" placeholder="Confirmação de senha">
      </div>
    </form>

    <div class="buttons">
      <button @click="emitirMostrarDados" class="btn btn-primary">Mostrar Dados do Usuário</button>
      <button @click="limparDados" class="btn btn-secondary">Limpar Dados</button>
    </div>
  </div>
</template>

<style scoped>
.form-container {
  width: 80%;
  max-width: 1200px;
  margin: auto;
  padding: 20px;
  background-color: #f8f9fa;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.edit {
  display: flex;
  flex-direction: column;
}

.form-group {
  margin-bottom: 15px;
}

.form-group label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

.form-control, .form-select {
  width: 100%;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #ced4da;
}

.form-control:focus, .form-select:focus {
  border-color: #80bdff;
  outline: none;
}

.buttons {
  display: flex;
  justify-content: space-between;
}

.btn {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  cursor: pointer;
}

.btn-primary {
  background-color: #007bff;
  color: #fff;
}

.btn-secondary {
  background-color: #6c757d;
  color: #fff;
}

.btn-primary:hover {
  background-color: #0056b3;
}

.btn-secondary:hover {
  background-color: #5a6268;
}
</style>