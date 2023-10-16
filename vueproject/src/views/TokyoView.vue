<template>
    
    <body> 
    
        <HeaderMenu />
     
      <header class="banner">
        <RouterLink to="/"> <i class="fa-solid fa-arrow-left"></i></RouterLink>
        <section class="container">
        <div class="slider-wrapper">
            <div class="slider">
                <img id="slide-1" src="../components/images/tokyo1.jpg"/>
                <img id="slide-2" src="../components/images/tokki.jpg"/>
                <img id="slide-3" src="../components/images/tokyio.jpeg"/>
            </div>
            <div class="slider-nav">
                <a href="#slide-1"></a>
                <a href="#slide-2"></a>
                <a href="#slide-3"></a>
            </div>
        </div>
    </section>
      </header>
      <br>
      <main>
      <h1>Tokyo</h1>
      <p class="visit"><i class="fa-solid fa-calendar-days"></i> visited 10/1 - 20/8/23</p>
      <span><i class="fa-solid fa-user"></i> by Saron </span>
    </main>
    <br>
      <div class="textblock">
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Unde odit inventore exercitationem
          ipsa, repellat laborum necessitatibus quidem ipsum sunt consequuntur amet voluptatem pariatur
          corporis architecto, et iusto aspernatur alias dolore. Lorem, ipsum dolor sit amet consectetur
          adipisicing elit. Reprehenderit nesciunt delectus quaerat esse deleniti et officiis ex
          laboriosam, rem soluta repellat hic magnam accusantium voluptatem beatae nostrum minima quia
          quas!
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Unde odit inventore exercitationem
          ipsa, repellat laborum necessitatibus quidem ipsum sunt consequuntur amet voluptatem pariatur
          corporis architecto, et iusto aspernatur alias dolore. Lorem, ipsum dolor sit amet consectetur
          adipisicing elit. Reprehenderit nesciunt delectus quaerat esse deleniti et officiis ex
          laboriosam, rem soluta repellat hic magnam accusantium voluptatem beatae nostrum minima quia
          quas!
        </p>
      </div>
      <div class="map">
        <MapBox/>
      </div>
    
    </body> 
    <span class="social">
    <SocialMedia/>
      </span>
    </template>
    
    <script>
    import HeaderMenu from '../components/HeaderMenu.vue'
    import MapBox from '../components/MapBox.vue';
    import SocialMedia from '../components/SocialMedia.vue';
    
    export default {
      components: { HeaderMenu, MapBox, SocialMedia }
    }
    </script>
    
    <style scoped>
    
    
    .banner {
      margin-top: 200px;
      top: 0;
    }
    .banner i{
  font-size: 20pt;
  margin-left: 20px;
}
    div.textblock {
      display: flex;
      flex-direction: row;
      /* gap: 50px; */
    }
    .textblock p {
      margin-top: 50px;
      letter-spacing: 3px;
      margin-left: 100px;
      margin-right: 100px;
      margin-bottom: 260px;
    }
    h1 {
      font-family: myFont;
      margin-bottom: 20px;
      letter-spacing: 2px;
    }
    
    i{
      margin-top: 10px;
      margin-bottom: 10px;
    }
    main{
      text-align: center;
      letter-spacing: 1px;
      margin-bottom: 40px;
    }
    
    span.social{
    bottom: 0;
    margin-right: 5px;
    }
    .container {
        padding: 2rem;
    }
    
    .slider-wrapper {
        
        max-width: 48rem;
        margin: 0 auto;
    }
    
    .slider {
        display: flex;
        aspect-ratio: 21 / 9;
        overflow-x: auto;
        scroll-snap-type: x mandatory;
        scroll-behavior: smooth;
        box-shadow: 0 1.5rem 3rem -0.75rem hsla(0, 0%, 0%, 0.25);
        border-radius: 0.5rem;
        -ms-overflow-style: none; 
        scrollbar-width: none; 
    }
    
   
    .slider::-webkit-scrollbar {
        display: none;
    }
    
    .slider img {
        flex: 1 0 100%;
        scroll-snap-align: start;
        object-fit: cover;
    }
    
    .slider-nav {
        display: flex;
        column-gap: 1rem;
        position: relative;
        bottom: 2.25rem;
	      left: 100%;
	      transform: translateX(-50%);
        z-index: 1;
    }
    
    .slider-nav a {
        width: 0.5rem;
        height: 0.5rem;
        border-radius: 50%;
        background-color: #fff;
        opacity: 0.75;
        transition: opacity ease 250ms;
    }
    
    .slider-nav a:hover {
        opacity: 1;
    }
    @media screen and (max-width: 990px){
  .slider-nav{
    bottom: 9.25rem;
  }

}
    </style>
    