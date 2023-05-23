<template>
	<HelloWorld :name="name" :age="age" />
	<input type="text" v-model='name' /><br>
	<input type="text" v-model='age' />
</template>

<script setup>
import HelloWorld from "@/components/HelloWorld.vue";
import { ref } from "vue";

const name = ref('GrCOTE7');
const age = ref(58);

const display = () => {
  console.log(name.value, age.value)
}

display()
</script>

<style scoped></style>
