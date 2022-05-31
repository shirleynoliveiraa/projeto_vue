<template>
  <h1>Meu nome é: {{ name }}</h1>
</template>

<script>
export default {
  name: 'LifeCycle',
  data() {
    return {
      name: 'Ainda não sei'
    }
  },
  created() {
    setTimeout (() => {
      this.name = 'Joao'
    }, 1000);
    this.lifeCycle()
  },
  mounted() {
    setTimeout (() => {
    this.name = 'Pedro'
    }, 2000);
    this.lifeCycle()
  },
  methods: {
    lifeCycle() {
      console.log("Executou");
    }
  }
}
</script>