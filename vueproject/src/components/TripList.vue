<template>
  <div class="trip-gallery">
    <div>
      <RouterLink to="enoshima">
        <h1>Enoshima</h1>
        <p><i class="fa-solid fa-calendar-days"></i> 1/8 - 6/8/23</p>
        <span><i class="fa-solid fa-user"></i> by Saron </span>
      </RouterLink>
    </div>

    <div>
      <RouterLink to="kyoto">
        <h1>Kyoto</h1>
        <p><i class="fa-solid fa-calendar-days"></i> 6/8 - 10/8/23</p>
        <span><i class="fa-solid fa-user"></i> by Saron </span>
      </RouterLink>
    </div>

    <div>
      <RouterLink to="tokyo">
        <h1>Tokyo</h1>
        <p><i class="fa-solid fa-calendar-days"></i> 10/8 - 20/8/23</p>
        <span><i class="fa-solid fa-user"></i> by Saron </span>
      </RouterLink>
    </div>

    <div>
      <RouterLink to="hokkaido">
        <h1>Hokkaido</h1>
        <p><i class="fa-solid fa-calendar-days"></i> 20/8 - 31/8/23</p>
        <span><i class="fa-solid fa-user"></i> by Saron </span>
      </RouterLink>
    </div>
  </div>
</template>

<script>
import { RouterLink } from 'vue-router'

export default { components: { RouterLink } }
</script>

<style scoped>
div .trip-gallery {
  display: flex;
  margin-top: 180px;
  margin-bottom: 100px;
  margin-left: 10px;
  gap: 10px;
}
img {
  object-fit: cover;
  width: 100%;
}

.trip-gallery div {
  color: black;
  border-radius: 20px;
  /* From https://css.glass */
  background: rgba(255, 255, 255, 0);
  border-radius: 150px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  padding: 30px 50px 0px 50px;
  justify-content: center;
  text-align: center;
  gap: 20px;
  transition: 0.5s;
  position: relative;
  height: 40vh;
}
.trip-gallery div:hover {
  transform: scale(1.2);
}

@font-face {
  font-family: myFont;
  src: url('icons/Rosalia.otf');
}
.trip-gallery div:nth-child(1) {
  background-image: url('../components/images/en.png');
  background-repeat: no-repeat;
  background-size: 100% 50%;
}
.trip-gallery div:nth-child(2) {
  background-image: url('../components/images/ky.png');
  background-repeat: no-repeat;
  background-size: 100% 50%;
}
.trip-gallery div:nth-child(3) {
  background-image: url('../components/images/to.png');
  background-repeat: no-repeat;
  background-size: 100% 50%;
}
.trip-gallery div:nth-child(4) {
  background-image: url('../components/images/ho.png');
  background-repeat: no-repeat;
  background-size: 100% 50%;
}
h1 {
  font-family: myFont;
  padding-top: 140px;
  font-size: 19px;
}
h1,
p,
span {
  text-align: center;
  margin-top: 25px;
  letter-spacing: 1px;
}
@media screen and (max-width: 990px){
  div .trip-gallery{
    display: block;
  }
}
</style>
