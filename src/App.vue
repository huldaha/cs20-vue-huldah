<template>
	<div class="container">
		<MyHeader />
		<HelloWorld />
	</div>
</template>
<script>
//sub-component must be imported and then registered in "components" below
import MyHeader from "./components/MyHeader.vue";
import HelloWorld from "./components/HelloWorld.vue";

export default {
	components: { MyHeader, HelloWorld },
};
</script>

<style scoped>
body {
	background-color: rgb(243, 255, 255);
}
.container {
	margin: 8px;
}
</style>
