<template>
  <main>
      <div class="bg-container">
        <div class="content">
            <ProductCard v-for="(elemento,i) in dcLista" 
            :key="i"
            :img="elemento.thumb"
            :prezzo="elemento.price"
            :title="elemento.series"
            :subtitle="elemento.type"
            >
            </ProductCard>
         </div>
      </div>



      <section class="section-icon">
      <div class="icon-container">
          <div v-for="(el,i) in servizi" :key="i" class="flex-style">
              <img class="icon-style" :src="require('../assets/'+ el.pic)"  alt="">
              <p class="icon-text" >{{el.servizio}}</p>
          </div>
         
          
          
        
      </div>
      </section>

      
  </main>
</template>

<script>
import ProductCard from "@/components/griglia.vue";
import jsonData from "../assets/dc-comics.json";
export default {

    
    name: "Main",
    components:{
        ProductCard
    },

    data(){
        return{

            dcLista : jsonData,
            servizi:[
                {
                    servizio: "Digital Comics",
                    pic: "buy-comics-digital-comics.png",
                },
                   {
                    servizio: "Dc Merchandaise",
                    pic: "buy-comics-merchandise.png",
                },
                    {
                    servizio: "Subscrition",
                    pic: "buy-comics-subscriptions.png",
                },
                 {
                    servizio: "Comic Locator Shop",
                    pic: "buy-comics-shop-locator.png",
                },
                   {
                    servizio: "Dc Power Visa",
                    pic: "buy-dc-power-visa.svg",
                },
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
    @import "../style/main.scss";
</style>