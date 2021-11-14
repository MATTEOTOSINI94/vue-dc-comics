<template>
  <header class="hello">
    <div class="container-logo-list">
      <div>
        <img src="../assets/dc-logo.png" alt="">
      </div>

        <ul>
          <li v-for="(elemento,i) in service" :key="i" :class="i === currentActive ? 'marker' : '' "  @click="currentActive = i">{{elemento.titolo}}</li>
          
        </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',

  data(){
    return{

      currentActive:0,
      service:[
        {
          titolo:"CARACHTER"
        },
          {
          titolo:"COMICS"
        },
          {
          titolo:"MOVIES"
        },
          {
          titolo:"TV"
        },
          {
          titolo:"GAME"
        },
          {
          titolo:"VIDEOS"
        },
                  {
          titolo:"FANS"
        },
                 {
          titolo:"NEWS"
        },
        {
          titolo:"SHOP"
        }
      ]
    }
  }
 
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
   @import "../style/header";
</style>
