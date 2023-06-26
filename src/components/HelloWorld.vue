<script setup lang="ts">
import { chunk } from 'loadsh'
import { reactive } from 'vue'

defineProps<{ msg: string }>()

let data = reactive({
  num: 0
})
const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
console.log(chunk(arr));
function addd() {
console.log(chunk(arr, data.num));
}

function asdd(params: Array<number>) {
  console.log([...params]);
}
function asdds() {
  console.log([...arguments]);
}

asdds.apply(arr)

</script>

<template>
  <input v-model="data.num" type="number">
  <div>{{ data.num }}</div>
  <button @click="addd">addddd</button>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
