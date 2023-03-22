<template>
  <div>
    <p> Página Inicial </p>
    <form @submit.prevent="receberDados">
      <input v-model="inputNome" type="text" name="nome" id="nome">
      <button> Enviar </button>
    </form>
    <ul>
      <li v-for="name in names"> {{ name }} </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      names: [],
      inputNome: ""
    }
  },
  methods: {
    receberDados(){
      console.log(this.inputNome)
      this.names.push(this.inputNome)
    }
  }
}
</script>