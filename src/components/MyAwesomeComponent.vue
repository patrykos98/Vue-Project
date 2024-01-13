<template>
  <div>
    <ChildComponent :textprops="text"/>  
  </div>
</template>

<script>
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

export default {
    name: "MyAwesomeComponent",
    setup() {
        const text = ref('Testujemy propsa :D');
        const liczba = ref(1);
        const isShow = true;
        return { text, liczba, isShow };
    },
    components: { ChildComponent }
}

</script>


