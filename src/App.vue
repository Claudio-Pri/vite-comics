<script>
/*
Passaggi import componente:
1) Importazione componente
2) Dichiarazione del componente
3) Utilizzo del componente
*/

// 1) Importazione componente
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

  export default {
  data() {
    return { 
      
     }
  },
  //2) Dichiarazione del componente (prima o dopo data())
  components: {
    AppHeader,
    AppMain,
  },
  methods: {
    
  }
}
</script>

<template>
  <!-- N.B. Template vuole 1 solo figlio -->
  <div>
    <!-- 3) Utilizzo del componente come tag htm (self-closing) -->
    <AppHeader/>

    <AppMain/>
    
    
    <footer>Footer</footer>
    
  </div>
</template>

<style lang="scss" scoped>
// npm install -g sass
// @use 'assets/scss/main.scss' as *;
// @use 'assets/scss/variables.scss' as *;

</style>
