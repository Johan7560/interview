<script setup lang="ts"></script>

<template>
	<nav class="footer absolute flex justify-center rounded-b-2xl bg-white">
		<div class="flex px-6 text-center not-italic">
			<div class="w-28">
				<font-awesome-icon icon="gear" />
				<p class="navText">Projects</p>
			</div>
			<div class="w-28">
				<font-awesome-icon icon="gear" />
				<p class="navText">Customers</p>
			</div>
			<div class="w-28">
				<font-awesome-icon icon="gear" />
				<p class="navText">Company</p>
			</div>
		</div>
	</nav>
</template>

<style scoped>
.footer {
	width: 375px;
	height: 56px;
	top: 836px;
	border-top: 1px solid rgba(0, 13, 26, 0.08);
	font-family: 'Inter';
	padding: 9px 24px;
	gap: 4px;
}
.navText {
	font-size: 10px;
	font-weight: 450;
	font-style: normal;
	color: rgba(0, 0, 0, 0.7);
	font-variation-settings: 'slnt' 0;
	line-height: 12px;
	font-family: 'Inter';
}
</style>
