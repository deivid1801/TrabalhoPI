<script setup>
import { ref } from 'vue'
const texto = ref('')





</script>

<template>
  <form>
  <div class="row">
    <div class="col">
      <input  type="text" v-bind:value="texto" v-on:input="event => texto = event.target.value" class="form-control" placeholder="Enter email" name="email ">
      <input type="text" class="form-control" placeholder="insira seu nome">
      <input type="text" class="form-control" placeholder="insira sua data de nascimento">
      <input type="text" class="form-control" placeholder="insira seu endereço">
      <input type="text" class="form-control" placeholder="insira sua cidade">
      <p>Texto digitado: {{ texto }}</p>

      <p>insira seu Estado</p>

     <select class="form-select mt-3">
     <option>AC</option>
     <option>AL</option>
     <option>AP</option>
     <option>AM</option>
     <option>BA</option>
     <option>CE</option>
     <option>DF</option>
     <option>ES</option>
     <option>GO</option>
     <option>MA</option>
     <option>MT</option>
     <option>MS</option>
     <option>MG</option>
     <option>PA</option>
     <option>PB</option>
     <option>PR</option>
     <option>PE</option>
     <option>PI</option>
     <option>RJ</option>
     <option>RN</option>
     <option>RS</option>
     <option>RO</option>
     <option>RR</option>
     <option>SC</option>
     <option>SP</option>
     <option>SE</option>
     <option>TO</option>
   </select>
   <input type="text" class="form-control" placeholder="insira seus Hobbies
">
   <input type="text" class="form-control" placeholder="insira suas Linguagens de programação
">
   <input type="text" class="form-control" placeholder="insira sua Biografia">


    </div>
    <div class="col">
      <input type="password" class="form-control" placeholder="insira sua senha" name="pswd">
      <input type="password" class="form-control" placeholder="confirmaçao de senha" name="pswd">

      
    </div>
  </div>
</form>
</template>

<style scoped>

</style>
