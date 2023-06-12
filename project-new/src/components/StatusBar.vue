<template>
	<div class="iconsBar flex h-11 justify-between p-4">
		<div class="time">{{ currentTime() }}</div>
		<div class="icon">
			<span class="bars">
				<font-awesome-icon icon="signal" />
			</span>
			<span class="signal">
				<font-awesome-icon icon="wifi" />
			</span>
			<span class="battery">
				<font-awesome-icon icon="battery-full" />
			</span>
		</div>
	</div>
</template>

<script lang="ts">
import moment from 'moment';

export default {
	computed: {},
	methods: {
		currentTime() {
			moment.locale('af');
			return moment().format('LT');
		}
	}
};
</script>

<style>
.iconsBar {
	width: 375px;
}

.time {
	width: 74px;
	height: 18px;
}

.icon span {
	padding-left: 4px;
}
</style>
