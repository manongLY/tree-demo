<template>
  <ul class="tree-body">                                    
    <li v-for="item in list" :id="item.id">
      <div>
        id:{{item.id}}
        count: {{item.clickCount}}
        <button @click="add(item)">+1</button>
      </div>      
      <tree :list="item.children"></tree> 
    </li>
  </ul>
</template>

<script setup>
defineProps({
  list: Array
})

function add(item){
  ++item.clickCount
}
</script>

<style>
.tree-body{
  margin: 10px 30px 0;
}
</style>