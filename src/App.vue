<template>
  <div id="app">

    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

    <h1>Sistema de Cadastro</h1>

    <div class="container">
      <div class="div" v-bind:key="cadastro.id" v-for="cadastro in cadastros">
        <p>Cadastro ID: {{cadastro.id}}</p>
        <p>Descrição: {{cadastro.descricao}}</p>
        <p v-if="cadastro.estaCompleta" id="completo">CADASTRO CONCLUÍDO</p>
        <p v-else id="incompleto">CADASTRO INCOMPLETO</p>
      </div>
    </div>
    

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  },
  data(){
    return {
          cadastros: [
            {id: 1, descricao: "Descrição 111111", estaCompleta: true},
            {id: 2, descricao: "Descrição 222222", estaCompleta: false},
            {id: 3, descricao: "Descrição 333333", estaCompleta: false},
            {id: 4, descricao: "Descrição 4444444", estaCompleta: true},
            {id: 5, descricao: "Descrição 5555555", estaCompleta: true},
            {id: 6, descricao: "Descrição 666666", estaCompleta: false},
          ]
    }

  }
  // filters: {
  //   verificaComplemento: function(item){
  //     return item.toUpperCase();
  //   }
  // }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.div{
  /* border: palevioletred 1px solid; */
  width: 300px;
  height: 250px;
}

.container{
  display: flex;
  justify-content: center;
  width: 90%;
  flex-wrap: wrap;
}

#completo{
  color: green;
  font-weight: bolder;
  font-size: 1.1em;
}

#incompleto{
  color: orange;
  font-weight: bolder;
  font-size: 1.1em;
}
</style>
