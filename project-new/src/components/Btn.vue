<template>
	<button
		class="addingIcon border-1 absolute ml-4 flex h-12 items-center justify-center border-solid border-black"
	>
		<i class="plusIcon leading-5"><font-awesome-icon icon="plus" /></i>
		<p class="font-semibold leading-5">New Project</p>
	</button>
</template>

<script lang="ts">
export default {
	computed: {},
	methods: {
		handleForm() {
			console.log('yoyo');
		}
	}
};
</script>

<style scoped>
.addingIcon {
	width: 343px;
	padding: 10px 28px 12px 20px;

	top: 778px;

	background: #0055ff;
	border-radius: 28px;

	box-shadow: 0px 0px 0px 1px rgba(0, 0, 0, 0.03), 0px 1px 2px rgba(0, 0, 0, 0.05),
		0px 4px 8px rgba(0, 0, 0, 0.1);
}

.plusIcon {
	width: 24px;
	height: 16px;
	color: #fff;
}

.addingIcon p {
	font-size: 16px;

	height: 20px;
	width: 94px;
	color: #fff;

	font-family: 'Inter';
	/* font-style: normal; */
}
</style>
