<script setup>
import Tree from './components/Tree.vue'
import { ref} from "vue"
let nodeData = ref({
    id: 1,
    clickCount: 1,
    children:[
        {
            id: 2,
            clickCount: 2,
            children: [
                {
                    id: 3,
                    clickCount: 3,
                    children: []
                }
            ]
        },
        {
            id: 5,
            clickCount: 2,
            children: [
                {
                    id: 6,
                    clickCount: 3,
                    children: []
                }
            ]
        }
    ]
})
</script>

<template>
  <Tree :list="[nodeData]"></Tree>
</template>

<style>
#app {
  margin-top: 60px;
}
</style>
