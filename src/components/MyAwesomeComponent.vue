<template>
   <div class="to-do-container">
    <div class="header">
      <h1>ToDo List</h1>
    </div>
    <div class="to-do-elements">
       <input type="text" placeholder="What you need to do?">
       <button @click="addElement">Dodaj</button>
    </div>
    
   </div>
</template>

<script>
//import { ref } from 'vue';

export default {
  name: 'MyAwsomeComponent',
  components: {
    
  },
  setup() {
    function addElement(){
      const divElement=document.querySelector('to-do-elements');
      //const liItem=document.createElement('li');
      //divElement.appendChild(liItem);
      console.log(divElement)
      
    }
    

    return { addElement};
  },
};
</script>

<style lang="scss">
body{
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  height: 100vh;
  width: 100vw;
  margin:0;
  padding:0;
  background-color: #99CCFF;
  background: linear-gradient(to right top, #99CCFF, #0066CC);
}

.to-do-container{
  display:flex;
  flex-direction: column;
  min-height: 45vh;
  min-width: 30vw;
  background-color: azure;
  box-shadow: 0px 0px 35px black;
  border-radius: 5px;
}

.header{
  align-self: center;
}

.to-do-elements{
  align-self: center;
}
</style>