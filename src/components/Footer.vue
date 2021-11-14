<template>
  <footer>
      <div id="bg-maxi-container">

          <div class="lista-container">
             <div class="conetent-list">
               
                <ul>  
                   <h3>DC Comics</h3>
                  <li v-for="elemento,i in dcomics" :key="i">{{elemento}}</li>
                 

              </ul>
            
                
                   
                      
                  <ul>
                     <h3>DC</h3>
                    <li v-for="el,i in shopDc" :key="i">{{el}}</li>
                    
                    
                  
                </ul>
                </div>
             
                   
                 <div class="lista-s">
                  <ul>
                    <h3>SITES</h3>
                    <li v-for="element,i in dc " :key="i">{{element}}</li>
                   
              </ul>
             
              
                  
                  
                  <ul>
                    <h3>SHOP</h3>
                    <li v-for="site,i in sites" :key="i">{{site}}</li>
                  
                    
              </ul>
             </div>
            
             

             
                 <img class="style-img" src="../assets/dc-logo-bg.png" alt="">
             
          </div>
      </div>
        <section class="final-section">

            <div class="last-tape">
                <div><button>SIGN-UP-NOW</button></div>
                <div class="icon-lastape">
                    <h3 class="stile">FOLLOW US</h3>
                 </div>

                   <div class="icon-img">
                       <img src="../assets/footer-facebook.png" alt="">
                        <img src="../assets/footer-periscope.png" alt="">
                        <img src="../assets/footer-pinterest.png" alt="">
                        <img src="../assets/footer-twitter.png" alt="">
                        <img src="../assets/footer-youtube.png" alt="">
                    </div> 
                        
                    
               
                
            </div>

        </section>


  </footer>


</template>

<script>
export default {
    name:"Footer",
    data(){
        return{
            dcomics:[
                "Caracherts",
                "Comics",
                "Movies",
                "Tv",
                "Games",
                "Videos",
                "News",
            ],

            shopDc:[
                "Shop DC",
                "Shop DC Collectibles"
            ],


            dc:[
                "Terms of use",
                "Privacy Policies",
                "Ad Choiches",
                "Jobs",
                "Subscrition",
                "Talenet WorkShop",
                "CpSc Certificate",
                "Ratings",
                "Shop Help",
                "Contact Us"
            ],

            sites:[
                "DC",
                "Mad Magazine",
                "Dc Kids",
                "DC Universe",
                "DC Power Visa"
            ]
        
        }
    }

}
</script>

<style lang="scss" scoped >
     @import "../style/footer.scss";
</style>
    
