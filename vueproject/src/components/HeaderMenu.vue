<template>
  <nav>
    <ul>
      <li>
        <RouterLink to="/"><img src="../components/images/logo.png" alt="" /></RouterLink>
      </li>
      <li><b>around the world </b></li>
      <li><RouterLink to="contact">CONTACT</RouterLink></li>
      <li>
        <RouterLink to="#"><span>NEW POST</span></RouterLink>
      </li>
      <li><RouterLink to="login">LOG IN</RouterLink></li>
    </ul>
  </nav>
  
  <div class="toggel">
    <ul>
    <li>
        <RouterLink to="/"><img src="../components/images/logo.png" alt="" /></RouterLink>
      </li>
    <li><b>around the world </b></li>
    <li><i @click="toggleMobileNav" v-show="mobile" class="fa-solid fa-bars"></i></li>
  </ul>
  </div>
  <div v-show="MobileNav" class="dropdown">
    <ul>
      <li><RouterLink to="contact">CONTACT</RouterLink></li>
      <li>
        <RouterLink to="#"><span>NEW POST</span></RouterLink>
      </li>
      <li><RouterLink to="login">LOG IN</RouterLink></li>
    </ul>
  </div>
</template>

<script>
import { RouterLink } from 'vue-router'

export default {
  components: { RouterLink },
  data(){
    return{
      MobileNav: null,
      mobile:true

    };
  },
  methods:{
    toggleMobileNav(){
      this.MobileNav =! this.MobileNav
    }
  }
}
</script>

<style scoped>

nav ul li {
  list-style-type: none;
  display: inline;
}
nav {
  position: fixed;
  margin-bottom: 90px;
  margin-top: 30px;
 text-align: center;
}
nav ul li a {
  text-decoration: none;
  font-family: Quicksand, Helvetica, sans-serif;
  font-size: 15pt;
  color: black;
  margin-right: 20px;
  position: relative;
   text-decoration: none;
  font-size: 18px;
  letter-spacing: 0.5px;
  padding: 0 10px;
}
nav ul li img {
  width: 2%;
  margin-right: 20px;
  margin-top: 20px;
  margin-left: 20px;

}
nav li:nth-child(2) {
  font-family: myFont;
  margin-right: 150px;
  font-size: 44pt;
  border: black 1px;
  border-radius: 10px;
  margin-left: 350px;
}
@font-face {
  font-family: myFont;
  src: url('./components/icons/Rosalia.otf');
}
a:after{
    content: "";
    position: absolute;
    background-color: #ffffff;
    height: 3px;
    width: 0;
    left: 0;
    bottom: -10px;
    transition: 0.3s;
}
a:hover{
    color: #ffffff;
}
a:hover:after{
    width: 100%;
}

div.dropdown{
  display: none;
  position:fixed;
  right: 0rem;
  top: 90px;
  background: rgba(94, 53, 113, 0.1);
  backdrop-filter: blur(15px);
  border-radius: 10px;
  overflow: hidden;
  font-family: quicksand;
  transition: height 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275) ;
}
div.toggel li:nth-child(2){
  font-family: myFont;
  font-size: 25pt; 
  position: absolute;
  margin: 10px 190px 10px 290px;
}
div.toggel li b{
  text-align: center;
  position: fixed;
}
div.dropdown li img{
  text-align: center;
}
div.dropdown li{
  padding: 0.7rem;
  display: flex;
  align-items: center;
  justify-content: center;

}
.toggel img{
  width: 6%;
  position: fixed;
  margin-top: 15px;
}
.toggel i{
  position: fixed;
  text-align: right;
  right: 20px;
  font-size: 40pt;
}

.toggel{
text-align: center;
display: none;
}
.toggel ul{
  display: none;
 flex-direction: row;
 justify-content: center;
 list-style-type: none;


}

/*responsive design*/
@media screen and (max-width: 990px){
  nav{
    display:none;
  }
  div.toggel{
  display: flex;
}
div.dropdown{
  display: block;
  
}
.toggel ul{
  display: flex;
}


}
</style>
