<template>
   <div class="container-card">
               <div class="card">
                   <img :src= img alt="logo">
                   <h4>{{title}}</h4>
                   

                <div class="overlay"><p>{{subtitle}}+{{prezzo}}</p></div>
               </div>

          </div>
</template>

<script>
export default {
    name: "ProductCard",
    props:["img","prezzo","title","subtitle"]

}
</script>

<style lang="scss" scoped>
    .container-card{
        width: calc(100% / 6 );
           
       
       

        .card{
           
           position: relative;
            
            h4{
                color: white;
                font-size: small;
            }

            img{
              width:150px;
              height: 150px;
              
              object-fit: cover
                
              
            };

            .overlay{
                content: "";
                position: absolute;
                bottom: 0;
                left: 0;
                right: 0;
                background-color: #f2f0f8;
                
                width: 0%;
                height: 100%;
                transition: 2s ;
                
            }


        }
    }

    .card:hover .overlay{
        opacity: 0.5;
        width: 100%;
    }
</style>