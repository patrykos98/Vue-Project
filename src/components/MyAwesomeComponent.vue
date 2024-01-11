<template>
  <div></div>
</template>

<script>
import {onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted} from 'vue'

export default {
  name: 'MyAwesomeComponent',
  setup(){

    console.log('setup');

    onBeforeMount(()=>{
      console.log('onBeforeMount');
    });
    onMounted(()=>{
      console.log('onMounted');
    });
    onBeforeUpdate(()=>{
      console.log('onBeforeUpdate');
    });
    onUpdated(()=>{
      console.log('onUpdated');
    });
    onBeforeUnmount(()=>{
      console.log('onBeforeUnmount');
    });
    onUnmounted(()=>{
      console.log('onUnmounted');
    });

    return{};
  }
};
</script>


