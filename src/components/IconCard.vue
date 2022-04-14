<template>
	<div class="card">
		<img width="100" height="100" :src="image" />
		<p>{{ title }}</p>
	</div>
</template>

<script>
export default {
	//props let you pass in values as attributes.
	//You can uses these in the template in the same way
	//as Data() properties
	props: ["title", "image"],
};
</script>

<style scoped>
p {
	margin: 0;
	font-weight: bold;
	font-family: sans-serif;
}
.card {
	display: flex;
	flex-direction: column;
	align-items: center;
	margin: 8px;
	padding: 4px;

	border-radius: 10px;
	background-color: white;
	box-shadow: 2px 2px 5px 2px rgb(201, 202, 230);
}
</style>
