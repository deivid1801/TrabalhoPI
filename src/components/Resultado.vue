<script setup>
import { ref } from 'vue'

const email = ref('')
const nome = ref('')
const dataN = ref('')
const endereço = ref('')
const cidade = ref('')
const estado = ref('')
const Hobbies = ref('')
const Linguagens = ref('')
const Biografia = ref('')
const senha = ref('')
const confirmaçao = ref('')
const botaoDados = ref('')
function limpardados (){
  email.value = ""
  nome.value = ""
  dataN.value = ""
  endereço.value = ""
  cidade.value = ""
  estado.value = ""
  Hobbies.value = ""
  Linguagens.value = ""
  Biografia.value = ""
  senha.value = ""
  confirmaçao.value = ""
  botaoDados.value = false
}

</script>
<template>
<button v-on:click="botaoDados = true " class="bot1">mostrar dados do usuario</button>
<button @click="limpardados" class="bot2"> limpar dados</button>

<div v-if = "botaoDados" class="dados">
<h4>dados usuario</h4>
    <p>email digitado: {{ email }}</p>
<p>nome digitado:{{ nome }}</p>
<p>data de nascimento digitado:{{ dataN }}</p>
<p>endereço digitado:{{ endereço }}</p>
<p>cidade digitado:{{ cidade }}</p>
<p>estado digitado:{{ estado }}</p>
<p>Hobbies digitado:{{ Hobbies }}</p>
<p>Linguagens digitado:{{ Linguagens }}</p>
<p>biografia digitado:{{ Biografia }}</p>
<p>senha digitado:{{ senha }}</p>
<p>confirmaçao digitado:{{ confirmaçao }}</p>
</div>
</template>
<style scoped>
.bot1{
  margin-left: 200px;
  background-color: rgb(160, 165, 173);
  border-radius: 10px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;

}
.bot2{
  background-color: rgb(160, 165, 173);
  border-radius: 10px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}
.dados{
  margin-left: 200px;
  background-color:rgb(187, 231, 231);
  margin-right: 130px;
}
.form-control{
  font: italic;
}
</style>