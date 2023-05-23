<template>
	<HelloWorld :user="user" />
	<input type="text" v-model='user.name' /><br>
	<input type="text" v-model='user.age' />
</template>

<script setup>
import HelloWorld from "@/components/HelloWorld.vue";
import { ref } from "vue";

const user = ref({
  name: 'GrCOTE7',
  age: 58
});

const display = () => {
  console.log(user.value)
}

display()
</script>

<style scoped></style>
