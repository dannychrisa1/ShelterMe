<template>
    <div class="details">
        <div class="container">
            <div class="col-md-12" v-for="(product,index) in items" :key="index">
                <div v-if="proId == product.productId">
                    <h1>{{product.name}}</h1>
                     <p>{{product.details}}</p>
                    <img :src="product.img" class="img-fluid">
                     <div class="row pl-4">
                         <div class="col-4">
                             a
                         </div>
                          <div class="col-4">
                              b
                         </div>
                          <div class="col-4">
                              c
                         </div>
                     </div>
                </div>
             </div>
         </div>     
    </div>
    
</template>
<script>
export default {
    name:'details',
    data(){
        return{
            proId: this.$route.params.Pid,
            title:"details",
             items:[
                {
                     productId: 1,
                    name:"Nestor's Villa",
            img:require("@/assets/car-1.jpg"),
            details:"Located at the heart of the city",
            btn:"Rent now",
            colus:{
                name:"take",
                color:"make",
            },

                },
                {
                   productId:2,
            name:"Danny's Villa",
           img:require("@/assets/car-2.jpg"),
           details:"Located at the heart of the city",
          btn:"Rent now"
                },
                {
                   productId: 3,
            name:"Rex House",
             img:require("@/assets/car-3.jpg"),
              details:"Located at the heart of the city",
              btn:"Rent now"
                },
                  {
                   productId: 4,
            name:"Banana lodge",
             img:require("@/assets/car-3.jpg"),
              details:"Located at the heart of the city",
              btn:"Rent now"
                },


            ],
                colors: [
          'indigo',
          'red',
          'blue',
          'green',
          'deep-purple accent-4',
        ],
        slides: [
          'First',
          'Second',
          'Third',
          'Fourth',
          'Fifth',
        ],
        }
    }
}
</script>