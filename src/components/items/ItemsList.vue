<template>
<div class="items-list">
    <SingleItem
    v-for="(item, index) in items"
      :key="item.id"
      :index="index"
      :item="item"
      :first-name="item.firstName"
      :last-name="item.lastName"
      :age="item.age"
    />
  </div>
</template>

<script>
import SingleItem from './item/SingleItem.vue'

export default{
    name:'ItemsList',
    components:{SingleItem},
    props:{
        items:{
            type:Array,
            default:()=>([])
        }
    }
}

</script>

<style lang="scss" scoped>
.items-list {
  font-family: arial;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 25px;
  max-width: 1200px;
  margin: 0 auto;
}
</style>