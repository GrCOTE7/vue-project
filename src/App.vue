<template>
	<HelloWorld />
	<div :class="[user.age < 18 ? 'text-red': 'text-green' ]">
		{{ user.name }}
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

<style scoped>
.text-red {
	color: indianred;
}
.text-green {
	color: green;
}
</style>
