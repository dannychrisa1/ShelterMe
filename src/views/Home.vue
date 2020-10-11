<template>
 <div>
   <div class="bgimg d-block d-md-block"
   :style="{backgroundImage: `url(${backgroundUrl})`}">
    <section class="top">
      <h1><span>Lets find a home</span> that's perfect for you</h1>
      <p class="d-none d-md-block">Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae corrupti ipsum dolorum. Distinctio vero repellat eveniet laboriosam, nobis culpa magni.</p>
      <div class="form-container">
        <form action="">
          <div class="form-left">
            <label for="location">Enter Your Location:</label>
            <input type="text" name="location" id="location" placeholder="Find house now">
            <i class="fa fa-search"></i>
            <p>Eg: "Abia"</p>
          </div>
        
        </form>

      </div>
    </section>
  </div>
  <section class="categories-m d-block d-md-none">
    <div class="pb-2 pt-2"><h6>Categories</h6></div>
    <div class="categories-content text-center">
      <div class="row">
        <div class="col-4">
          <i class="fa fa-university"></i>
          <div class="pt-2 title">flat</div>
        </div>
         <div class="col-4">
          <i class="fa fa-home"></i>
          <div class="pt-2 title">house</div>
        </div>
         <div class="col-4">
           <i class="fa fa-university"></i>
          <div class="pt-2 title">Room</div>
        </div>
      </div>
    </div>
  </section>
  <section class="properties-m d-block d-md-none">
    <div class="pb-2 pt-2"><h6>Top Properties</h6></div>
    <div class="properties-content" v-for="(data,index) in items" :key="index">
      <div class="row">
        <div class="col-4">
          <img :src="data.img" class="img-fluid"/>
        </div>
        <div class="col-8">
          <h6>{{data.name}}</h6>
          <p>{{data.details}}</p>
          <button class="btn btn-success"  @click="goTodetail(data.productId)">{{data.btn}}</button>

       </div>
     </div>
    </div>
  </section>
  
  <!-- <section class="over-view">
    <div class="right-col">
      <h2>About ShelterMe</h2>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Illum dignissimos asperiores sapiente fugit unde officiis labore a consectetur facilis minima!</p>
    </div>
    <img :src="car" class="img-fluid"/>
  </section>  -->

 

 </div>
</template>

<script>
  import backgroundUrl from "@/assets/computerBU.jpg";
  import car from "@/assets/car-4.jpg";

  export default {
    name: 'Home',
    data(){
      return{
            backgroundUrl,
            car,
        items:[
          {
            productId: 1,
            name:"Nestor's Villa",
            img:require("@/assets/car-1.jpg"),
            details:"Located at the heart of the city",
            btn:"Rent now"
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
    

        
      }
    },
    methods:{
      goTodetail(proId){
        this.$router.push({name:'details', params: {Pid:proId}})
      }
    }
  }
</script>
