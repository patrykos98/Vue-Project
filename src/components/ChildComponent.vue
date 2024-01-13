<template>
    <div>
        {{ textprops }}  
        <button @click="sendEvent"> Send </button>
    </div>
  </template>
  
  <script>
  
  export default {
    name: "ChildComponent",
    props:{
        textprops: 
        {
        type:String,
        required:true,
        default:'default value of props'
        }
    },
    setup(props,{emit}) {
         const sendEvent = ()=>{
            emit('firstLesson', '1. Wprowadzenie do frameworka')
         }

         return{sendEvent}
      }
    }
  
  </script>
  
  
  