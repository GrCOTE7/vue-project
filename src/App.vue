<template>
	<HelloWorld />

	<input type="text" v-model="name" />
	<input type="text" v-model="age" />
</template>

<script setup>
import HelloWorld from "@/components/HelloWorld.vue";
import { watch, ref } from "vue";

const name = ref("GrCOTE7");
const age = ref(17);

watch(name, (newValue, oldValue) => {
	console.log(newValue, oldValue);
});
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
