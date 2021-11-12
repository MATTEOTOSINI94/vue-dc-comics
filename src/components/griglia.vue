<template>
   <div class="ciao">
               <div class="card">
                   <img :src= img alt="logo">
                   <h4>{{title}}</h4>
                   <p>{{subtitle}}</p>
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
    .ciao{
        display: flex;
        flex-wrap: wrap;
        width: 100%;

        .card{
           width: calc(100% / 6);

            img{
                width: 100%
            };
        }
    }
</style>