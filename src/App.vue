<template>
  <div class="hello">

<div class="field">
  <h1>{{ count }}</h1>
</div>

<button class="btn" @click="increase">Increment</button>
<button class="btn" @click="decrease">Decrement</button>
    
  
  </div>
</template>

<script>

export default {
  name: 'App',

  data(){
    return{
      count:0,
    }
  },

  methods: {
    increase(){
      this.count=this.count+1;
    },

    decrease(){
      if(this.count <=0){
        this.count=0;
      }
      else{
        this.count=this.count-1;
      }
      
    }

  },
}
</script>

<style>
  .btn{
padding: 15px 20px;
background-color: rgb(65, 184, 131);
border: none;
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.5);
margin: 10px;

  }
  .btn:hover{
padding: 15px 20px;
background-color: rgb(60, 135, 101);
border: none;
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.5);
margin: 10px;
transition: 1s;

  }
  .field{

background-color: rgb(65, 184, 131);
border: none;
width:40%;
margin: 0 auto;

  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
