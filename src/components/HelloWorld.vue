<template>
	<div>
		<p>
			{{ msg }}
		</p>
		<p>
			This template is brought to you by:
			<!--use v-on:EVENTNAME to bind a method(function) to an event-->
			<button v-on:click="toggleIcons">
				<!--you can place any valid JS inside the {{ }}-->
				{{ !showIcons ? "Show" : "Hide" }} Icons
			</button>
		</p>

		<!--use v-if to conditionally render elements-->
		<div class="cardlist" v-if="showIcons">
			<!--use v-for to generate html elements for each
            item in an array or object-->
			<IconCard
				v-for="icon in icons"
				:title="icon.name"
				:image="icon.icon"
			/>
			<!--"props" defined in IconCard.vue let us pass in 
            the title and image path-->
		</div>
	</div>
</template>

<script>
import IconCard from "@/components/IconCard.vue";

export default {
	// reactive variables go inside the object returned by data()
	data() {
		return {
			msg: "Hello from the HelloWorld.vue file",
			showIcons: false,
			icons: [
				{
					name: "JCS CS",
					icon: "src/assets/RavenSquare.png",
				},
				{
					name: "VueJS",
					icon: "src/assets/VueLogo.png",
				},
			],
		};
	},
	components: { IconCard },
	methods: {
		toggleIcons() {
			//use this. to access data, props, and other methods
			this.showIcons = !this.showIcons;
		},
	},
};
</script>

<!--"scoped" means this css will only apply to this component,
so we can safely style <p> tags here without fear that it will
affect <p> tags in other components-->
<style scoped>
p {
	font-weight: bold;
	text-align: center;
}

.cardlist {
	display: flex;
	flex-direction: row;
	justify-content: center;
}
</style>
