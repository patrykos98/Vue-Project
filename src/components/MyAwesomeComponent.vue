<template>
  <div>
    <ChildComponent v-show="isShow" :textprops="text" @first-lesson="sendEvent"/> 
    <p>{{ lesson }}</p> 
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

        let lesson=ref('')

        const sendEvent= val =>{lesson.value=val}
        return { text, liczba, isShow, lesson, sendEvent };
    },
    components: { ChildComponent }
}

</script>


