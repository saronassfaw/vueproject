<template>
  <div>
    <HeaderMenu />
  </div>
  <main>
    <p>This project was made by</p>
    <img src="../components/images/me.png" alt="">
    <h1>Saron<br />Assfaw</h1>
    <a href="https://github.com/saronassfaw/vueproject"><i class="fa-brands fa-github"></i></a>
    <a href="https://hamburgcodingschool.com/"><p>hamburg coding school</p></a>
  </main>
  <SocialMedia />
</template>

<script>
import { RouterLink } from 'vue-router'
import HeaderMenu from '../components/HeaderMenu.vue'
import SocialMedia from '../components/SocialMedia.vue'
export default {
  components: { HeaderMenu, SocialMedia, RouterLink }
}
</script>

<style scoped>
h1 {
  font-family: myFont;
  font-size: 20pt;
  letter-spacing: 9px;
  text-align: center;
}
p {
  font-family: quicksand;
  letter-spacing: 1px;
}
i {
  font-size: 25pt;
  text-align: center;
}
i:hover{
  color: rgba(237, 240, 255, 0.507);
  transition: 0.5s;
}
img{
  width: 10%;
  text-align: center;
}
img:hover{
  width: 12%;
  transition: 0.4s;
}
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: auto;
  margin: auto;
}
@media screen and (max-width: 990px){

  img{
  width: 26%;
  text-align: center;
}
img:hover{
  width:29%;
  transition: 0.4s;
}

}
</style>
