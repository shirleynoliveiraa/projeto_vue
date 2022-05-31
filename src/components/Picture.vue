<template>
  <div>
    <img :src="avatar" :alt="descricao">
    <MudarImagem @mudar-imagem="trocarImagem" />
  </div>
</template>


<script>
import MudarImagem from './MudarImagem.vue'

export default {
  name: 'PictureVue',
  components: {
    MudarImagem
  },
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "nome da imagem"
    }
  },
  methods: {
      trocarImagem() {
        this.avatar = "/img/avatar2.png"
      }
    
  }
}
</script>