<template>
  <b-container class="border py-4" id="cont">
    <b-alert v-model="showAlert" dismissible>
      Email : {{ email }} / Mdp : {{ password }}
    </b-alert>
      <h2 class='mb-4'>Login</h2>
      <b-form-group>
        <b-form-input class='mb-1' v-model="email" placeholder="Enter Email" type="email">
        </b-form-input>
        <b-form-input class='mb-4' v-model="password" placeholder="Enter Password" type="password">
        </b-form-input>
        <b-button block variant="outline-success" @click="showAlert=true">Button</b-button>
        </b-form-group>
  </b-container>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      showAlert: false,
      email: '',
      password: ''
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#cont {
  max-width: 40%;
}
</style>
