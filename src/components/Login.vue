<template>
  <div class="card">
    <img src="../assets/logo.png" alt="Logo Train me">
    <b-field label="Email"
      :type="email.type"
      :message="email.message">
      <b-input 
        type="email"
        v-model="email.value"
        class="control">
      </b-input>
    </b-field>
    
    <b-field 
      label="Password"
      :type="password.type"
      :message="password.message">
      <b-input 
        type="password" 
        v-model="password.value"
        class="control"></b-input>
    </b-field>
    <a class="button is-info is-fullwidth">Log In</a>
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
  .card {
    padding: 5% 5% 5% 5%;
  }

  .title {
    padding: 8%;
  }
</style>
