<template>
  <header>
    <HeaderMenu />
  </header>
  <div class="box">
    <TripList />
    <MapBox />
  </div>
  <SocialMedia/>
</template>

<script>
import TripList from '../components/TripList.vue'
import HeaderMenu from '../components/HeaderMenu.vue'
import MapBox from '../components/MapBox.vue'
import SocialMedia from '../components/SocialMedia.vue';
export default {
  components: { TripList, HeaderMenu, MapBox, SocialMedia }
}
</script>

<style scoped>
div.box {
  display: flex; 
  margin-top: 100px;
  gap: 50px;
}
div.box:nth-child(2) {
  flex: 1;
  display: flex;
  /* position: relative; */
}
@media screen and (max-width: 990px){
  div.box{
    display: block;
  }
  div.box:nth-child(2) {
  flex: 3;
  display: flex;
  /* position: relative; */
}

}
</style>
