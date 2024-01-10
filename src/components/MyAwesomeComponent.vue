<template>
  <div>
    <p>Masks: {{ masks }}</p>
    <p v-if="masks>0">You can buy a mask!</p>
    <p v-if="masks<=0">You can not buy a mask, it's out of stock...</p>
    <button v-if="masks>0" @click="buyMask">Buy a mask</button>
  </div>
</template>

<script>
import {ref} from 'vue'

export default {
  name: 'MyAwesomeComponent',
  setup(){
    const masks =ref(5);
    
    function buyMask(){
      masks.value--;
    }
    return {masks, buyMask}
  }
};
</script>


