<template>
	<HelloWorld :user="user" />
	<input type="text" v-model="user.name" @input="display"/><br />
	<input type="text" v-model="user.age" /><br />
	
  <div v-if="user.age > 17">
    Je suis majeur
  </div>
  <div v-else>
    Je suis mineur
  </div>
   
</template>

<script setup>
import HelloWorld from "@/components/HelloWorld.vue";
import { reactive } from "vue";

const user = reactive({
	name: "GrCOTE7",
	age: 17,
});

const display = () => {
	console.log(user.name, user.age);
};

display();
</script>

<style scoped></style>
