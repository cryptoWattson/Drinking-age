<template>
  <div id="app">

    <!-- this is a comment -->

    
    <h1>Which Country Can I Drink In?</h1>

    <h2>Pick A Country</h2>

    <button @click="country='USA';age=''">USA</button>

    

    <button @click="country='Germany';age=''">Germany</button>


    <button @click="country='Japan';age=''">Japan</button>

    <h2>You Selected {{country}} </h2>

    <input v-model="age" type="number" placeholder="What is your age"> 

  <h1 v-show="candrink !== null">You can{{ candrink ? "":"not"}} drink</h1>
  </div>
</template>

<script>


export default {
  name: 'App',

  data: () =>{ 
    return { 
      country: "USA", 
      age: "",
      candrink: null,
    }
  },
 watch:{
   age(){
     this.age= parseInt(this.age)
     this.candrink= false;
     switch(this.country){
       case "USA":
         if(this.age>=21) this.candrink= true;
         break;
       case "Germany":
         if(this.age>=16) this.candrink= true;
         break;
       case "Japan":
         if(this.age>=20) this.candrink= true;
         break;
     }
     
     
   }
 }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
