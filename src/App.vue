<template>
  <HelloWorld />
  <span>{{ sentence }}</span>
  
  <input type="text" v-model="name">
  <input type="text" v-model="age">
</template>

<script setup>
import HelloWorld from "@/components/HelloWorld.vue";
import { computed, ref } from "vue";

const name = ref('GrCOTE7')
const age = ref(17);

const sentence = computed(()=>{
  return `Bonjour, je m'appelle ${name.value} et j'ai ${age.value} ans.`;
});
// console.log(sentence.value)
</script>

<style scoped>
.bold {
	font-weight: bolder;
}
.red {
	color: indianred;
}
.green {
	color: green;
}
</style>
