<template>
  <div
      class="single-item"
    >
      <p>Candidate {{ index + 1 }}</p>
      <p>Name: {{ firstName }} {{ lastName }}</p>
      <p>Age: {{ age }}</p>
      <p v-if="item.party">Party: {{ item.party }}</p>
      <div v-if="item.opinionPool">
        Opinion pool:
        <progress max="100" :value="item.opinionPool"></progress>
        {{ item.opinionPool }}%
      </div>
    </div>
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


