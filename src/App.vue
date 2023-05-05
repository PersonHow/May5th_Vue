<script>
import Caconetsu from './components/caconetsu.vue'
import guessNum from './components/guessNum.vue'
import seller from './components/seller.vue'


export default{
  components:{
    Caconetsu,
    guessNum,
    seller
  }
}
</script>

<template>
  <div class="containerr">
    <!-- <Caconetsu /> -->
    <!-- <guessNum /> -->
    <seller />
  </div>
</template>

<style scoped>
.containerr{
  width:100vw;
  height: 100vh;
  background-color: rgb(53, 102, 102);
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
