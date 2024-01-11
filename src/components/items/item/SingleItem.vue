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
export default{
    name:'SingleItem',
    props:{
        item:{
            type: Object,
            default:()=>({})
        },
        index:{
            type:Number,
            default:0
        },
        firstName:{
            type:String,
            default:''
        },
        lastName:{
            type:String,
            default:''
        },
        age:{
            type:Number,
            default:0
        }

    }
}
</script>

<style lang="scss" scoped>
.single-item {
    border: 1px solid black;
    padding: 10px;
  }

</style>