<template>
<div>
<h2>Meu Formulário</h2>
<form action="" @submit="enviarFormulario($event)">
  <div>
    <input type="text" :v-model="name">
  </div>
  <div>
        <input type="text" :v-model="email">
  </div>
  <div>
   <Submit />
  </div>
  </form>
  </div>
</template>

<script>
import InputText from './form/InputText.vue'
import Submit from './form/Submit.vue'

export default {
  name: 'FormVue',
  components: {
    InputText,
    Submit
  },
  data() {
    return {
      name: "Joao",
      email: "teste@teste.com"
    }
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault();
      
      const name = this.name;
      const email = this.email;

      console.log("Formulario enviado");
      console.log("O nome é: " + name);
      console.log("O email é: " + email);

      console.log( 'Formulario enviado');

      //o proximo passo seria uma requisicao assincrona
      //ajax ou fetch 
      //inserir no banco os dados
    }
  }
}
</script>