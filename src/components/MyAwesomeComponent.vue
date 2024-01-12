<template>
  <div>
    <div v-if="error">Something went wrong.</div>
    <Suspense>
    <template #default>
      <StarshipList/>
    </template>
    <template #fallback>
      <AppLoader/>
    </template>
    
  </Suspense>
  </div>
</template>

<script>
import{onErrorCaptured, ref} from 'vue'
import StarshipList from './StarshipList.vue'
import AppLoader from './AppLoader.vue';
export default {
  name: 'MyAwesomeComponent',
  components:{
    StarshipList,
    AppLoader
  },
  setup(){
    const error=ref(0)

    onErrorCaptured(e=>{
      error.value=e;
      return true;
    })
    
    return{error,onErrorCaptured}
  }
  }

</script>


