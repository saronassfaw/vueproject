<!-- <template>
    <div>
 <HeaderMenu/>

    </div>
    <main>
    <form @submit="submitForm">
        <h1>LOGIN</h1>
    <label for="" class="name" v-model="formValues.name"><b>NAME</b></label> <br>
    <input type="text" /><br>
    <label for="" class="password"><b>PASSWORD</b></label><br>
    <input type="password" /><br>
    <button type="submit" class="submit" @click="changeName" id="gbutton"><h2>LOG IN</h2></button>
  </form>
    </main>
    <footer>
    <SocialMedia/></footer>
</template>

<script>
import HeaderMenu from '../components/HeaderMenu.vue';
import SocialMedia from '../components/SocialMedia.vue';

    export default {
    components: { HeaderMenu, SocialMedia },
    data() {
    return {
      greeting: 'Hallo',
      counter: 0,
      formValues: {
      name: '',
      }
    }
  },
  methods:{
    changeName() {
      this.button = 'Nope not yet'
    },
    submitForm(event) {
      event.preventDefault()
      console.log('Form values', this.formValues)
  }
}

</script>

<style scoped>
main{
    margin-top: 200px;
    margin-left: 600px;
  
}
.name, .password{
font-family: quicksand;
    color: rgb(0, 0, 0);
    text-align: center;
    letter-spacing: 2px;
    padding-bottom: 30px;
}
h1{
    font-family: myFont;
    letter-spacing: 4px;
    font-size: 30pt;
    text-align: center;
    padding-bottom: 20px;
    padding-top: 20px;
}
.submit{
    background: rgba(255, 255, 255, 0);
  border-radius: 10px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  padding: 3px 70px 3px 70px;
  font-family: quicksand;
    margin-top: 20px;
  cursor: pointer;
  text-align: center;
}
.submit:hover{
    color: white;
    background-color: black;
    transition: 1s;
}

form{
    background: rgba(255, 255, 255, 0);
  border-radius: 20px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  padding: 30px 80px 50px 80px;
  text-align: center;
  margin-bottom: 100px;
}
input{
    border-radius: 10px;
    background: rgba(255, 255, 255, 0);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  margin-top: 10px;
  margin-bottom: 10px;
  padding: 10px 10px 10px 70px;
  margin-left: 20px;
  margin-bottom: 10px;
}
footer{
    padding-top: 40px;
}
</style> -->
<template>
  <div>
    <HeaderMenu />
    <main>
      <form @submit="submitForm">
        <h1>LOGIN</h1>
        <label for="name" class="name"><b>NAME</b></label> <br>
        <input type="text" v-model="formValues.name" id="name" /><br>
        <label for="password" class="password"><b>PASSWORD</b></label><br>
        <input type="password" id="password" /><br>
        <button type="submit" class="submit" @click="changeName"><h2>{{ login }}</h2></button>
      </form>
    </main>
    <footer>
      <SocialMedia />
    </footer>
  </div>
</template>

<script>
import HeaderMenu from '../components/HeaderMenu.vue';
import SocialMedia from '../components/SocialMedia.vue';

export default {
  components: { HeaderMenu, SocialMedia },
  data() {
    return {
      login: 'LOG IN',
      formValues: {
        name: '',
      },
    };
  },
  methods: {
    changeName() {
      this.login = 'IN PROGRESS'
    },
    submitForm(event) {
      event.preventDefault();
      console.log('Form values', this.formValues);
    },
  },
};
</script>

<style scoped>
main {
  margin-top: 200px;
  margin-left: 600px;
}

.name, .password {
  font-family: 'quicksand';
  color: rgb(0, 0, 0);
  text-align: center;
  letter-spacing: 2px;
  padding-bottom: 30px;
}

h1 {
  font-family: 'myFont';
  letter-spacing: 4px;
  font-size: 30pt;
  text-align: center;
  padding-bottom: 40px;
  padding-top: 20px;
}

.submit {
  background: rgba(255, 255, 255, 0);
  border-radius: 10px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  padding: 3px 70px 3px 70px;
  font-family: 'quicksand';
  margin-top: 20px;
  cursor: pointer;
  text-align: center;
}

.submit:hover {
  color: white;
  background-color: black;
  transition: 1s;
}

form {
  background: rgba(255, 255, 255, 0);
  border-radius: 20px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  padding: 30px 80px 50px 80px;
  text-align: center;
  margin-bottom: 100px;
  position: absolute;
}

input {
  border-radius: 10px;
  background: rgba(255, 255, 255, 0);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  margin-top: 10px;
  margin-bottom: 10px;
  padding: 10px 40px 10px 40px;
  margin-left: 20px;
  margin-bottom: 10px;
}

footer {
  padding-top: 40px;
}

@media screen and (max-width: 990px){
form{
  padding: 30px 70px 50px 70px;
  margin: 0 0 0 -500px;
  position: absolute;
}

}



</style>
