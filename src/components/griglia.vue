<template>
   <div class="container-card">
               <div class="card">
                   <div class="box-overlay">
                    <img :src= "img" alt="logo">
                      <div class="overlay"><p>{{subtitle}}+{{prezzo}}</p></div>
                   </div>
                   <h4>{{title}}</h4>
                   

              
               </div>

          </div>
</template>

<script>
export default {
    name: "ProductCard",
    // props:["img","prezzo","title","subtitle"]
    props:{

        img:{
            type: String,
            required: true
        },
         prezzo:{
            type: String,
            required: true
        },
         title:{
            type: String,
            required: true
        },
         subtitle:{
            type: String,
            required: true
        },

        active: Boolean,
    }



}
</script>

<style lang="scss" scoped>

  .box-overlay{
              position: relative;
              height: 120px;

          }
    .container-card{
        display: flex;
       width: calc(100% / 6);
           
     
       

        .card{
              
           width: 120px;
          
           
            
            h4{
                color: white;
                font-size: 10px;
                font-family: 'Times New Roman', Times, serif;
                padding: 10px 0;
                }

            img{
              width:120px;
              height: 120px;
             
              object-fit: cover
                
              
            };

            .overlay{
                content: "";
                position: absolute;
                top: 0;
                bottom: 0;
                left: 0;
                right: 0;
                background-color: #f2f0f8;
                opacity: 0;
                transition: 2s ;

                p{
                    position: absolute;
                    bottom: 50%;
                    right: 50%;
                    transform: translate(50%, 50%);
                    text-align: center;
                }
                
            }


        }
    }

    .box-overlay:hover .overlay{
        opacity: 0.8;
      width: 100%;
    }
</style>