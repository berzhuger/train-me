<template>
  <div class="imagem">
    <div class="form">
      <img src="../assets/logo.png" alt="Logo Train me" class="logo">
      <b-field
        :type="email.type"
        :message="email.message">
        <b-input
          placeholder="E-mail"
          type="text"
          v-model="email.value"
          class="control">
        </b-input>
      </b-field>
      
      <b-field 
        :type="password.type"
        :message="password.message">
        <b-input
          placeholder="Senha"
          type="password" 
          v-model="password.value"
          class="control"></b-input>
      </b-field>
      <a class="button is-info is-fullwidth">Entrar</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'login',
  data () {
    return {
      email: {
        message: '',
        type: '',
        value: ''
      },
      password: {
        message: '',
        type: '',
        value: ''
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only 
https://train-me-potato-edition-v2-rodrigofazenda.c9users.io/#/ -->
<style style="scss">
  html, body {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
  }
  
  body {
    display: flex;
    align-items: stretch;
  }
  
  input {
    opacity: 0.8;
  }
  
  .input:active, .input:focus {
    border-color: #3498db;
  }
  
  .imagem {
    background-image: url('../assets/background-login.png');
    width: 100%;
    height: 100%;
    padding: 10% 0 0 0;
  }
  
  .form {
    height: 100%;
    width: 100%;
    width: 100vw;
    padding: 5px;
  }
  
  .form label {
    color: #3498db;
    text-align: center;
  }

  .card {
    padding: 5% 5% 5% 5%;
    opacity: 0.8;
  }

  .title {
    padding: 8%;
  }
  
  .logo {
    display: block;
    margin: auto;
    padding: 10px;
    opacity: 1;
  }
</style>
