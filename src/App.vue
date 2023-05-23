<template>
	<HelloWorld />
	<div class="bold" :class="[{ red: isMineur, green: !isMineur }]">
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

const isMineur = user.age < 18;

const display = () => {
	console.log(user.name, user.age);
};

display();
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
