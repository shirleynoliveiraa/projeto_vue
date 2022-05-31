<template>
<div>
 
  <primeiro-componente />
  <p>O dado do app é: {{ testando }}</p>
  <life-cycle />
  <Pessoa />
</div>  
</template>

<script>

import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import Header from './components/Header.vue'


export default {
  name: 'App',
  components: {
    
    PrimeiroComponente,
    LifeCycle,
    Pessoa,
   
  },
  data() {
    return {
      testando: "Teste"
    }
  }
}
</script>


<style>
body {
  background-color:#333 ;
  color: #fff;
}
</style>