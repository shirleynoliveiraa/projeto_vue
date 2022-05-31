<template>
<div>
  <h2>Esta é a descrição da pessoa: {{ nome }} </h2>
  <Info :email="email" :esta_trabalhando=true />
  <Form />

</div>
</template>

<script>
import Info from './Info' 
import Form from './Form'

export default {
  name: 'PessoaVue',
  components: {
    Info,
    Form
  },
  data() {
    return {
      nome: 'Mateus' ,
      email: 'teste@teste.com'
    }
  }
}
</script>