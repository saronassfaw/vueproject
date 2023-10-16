<template>
<div>
   <RouterLink to="#"><i class="fa-brands fa-youtube"></i></RouterLink> 
      <RouterLink to="#"><i class="fa-brands fa-instagram"></i></RouterLink> 
      <RouterLink to="#"><i class="fa-brands fa-discord"></i></RouterLink>
    </div>
</template>


<script>
import { RouterLink } from 'vue-router';

    export default {
    components: { RouterLink }
}
</script>

<style scoped>
div{
  width: 100%;
  height: 40px;
  padding-top: 10px;
  position: fixed;
  bottom: 0;
  left: 0;
  text-align: center;
  margin-bottom: 20px;
}
div i{
    width: 15%;
    font-size: 20pt;
}
i:hover{
    color: white;
    transition: 0.5s;
}

</style>