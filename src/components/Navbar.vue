<template>
<div class="">
   <div class="nav-switch d-md-none d-block">
            <a href="#" onclick="openSlideMenu()"><i class="fa fa-bars menu" aria-hidden="true"></i></a>
    </div>
        <!-- nav-section -->
        <nav class="nav-section">
            <div class="container">
                 
                <ul class="main-nav nav-right d-none d-md-block">
                   <li v-for="item in items" :key="item.id" class="nav-item">
                    <router-link class="nav-link" :to="`${item.page}`">{{item.text}}</router-link>
                </li>
                   <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Categories
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <a class="dropdown-item" href="#">Flat</a>
                      <a class="dropdown-item" href="#">Single Room</a>
                      <a class="dropdown-item" href="#">House</a>
                    </div>
                </li>
                <li class="nav-item">
                    <router-link class="nav-link" to="/contact">Contact</router-link>
                </li>
                <li class="nav-item">
                    <router-link class="nav-link" to="/signIn"><button class="btn btn login-button">Login</button></router-link>
                </li>
              
                    <li class="nav-item">
                        <router-link class="nav-link" to="/signUp"><button class="btn btn signup-button">Sign Up</button></router-link>

                     </li>
                
                </ul>
                    <div class="logo pt-3">
                    <h2>ShelterMe</h2>
                </div>
                 
              
            </div>
        </nav>
        <div id="side-menu" class="side-nav">
                 <a href = "#" class="btn-close" onclick="closeSlideMenu()">&times;</a>
               <li v-for="item in items" :key="item.id" class="nav-item-mobile"  onclick="closeSlideMenu()">
                    <router-link class="nav-link" :to="`${item.page}`">{{item.text}}</router-link>
                </li>
                 <li class="nav-item-mobile dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                      Categories
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                      <a class="dropdown-item" href="#">Flat</a>
                      <a class="dropdown-item" href="#">Single Room</a>
                      <a class="dropdown-item" href="#">House</a>
                    </div>
                </li>
                <li class="nav-item-mobile"  onclick="closeSlideMenu()"> 
                    <router-link class="nav-link" to="/contact">Contact</router-link>
                </li>

              
            </div>
 
   

  

    


</div>






</template>

<script>
export default{
    name:'Navbar',
    props:{
        msg:String
    },
    data(){
        return{
            items:[
                {id:0, text:'Home', page:'/home'},
                {id:1, text:'About', page:'/about'},
               
                

        ]
    }
},
    
}
</script>


<style>
nav a.router-link-active{
    /* background-color: palevioletred; */
    color:#3583ba !important;
  
}
.nav-item .nav-link{ 
    padding-top: 15px !important;
    padding-bottom: 15px !important
}
</style>