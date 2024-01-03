<!-- 
  route params 
 -->
<template>
	<div class="p-5">
		Event id:
		<strong class="p-4 text-red-500">
			{{ $route.params.id }}
		</strong>
	</div>
</template>

<script>
export default {
	// fetch data on client-side
	data() {
		return {
			// id: this.$route.params.id,
		};
	},
	// fetch data on server-side
	asyncData({ params }) {
		return {
			id: params.id,
		};
	},

	mounted() {
		console.log('mounted', this.$route);
	},
};
</script>
