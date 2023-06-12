<template>
	<StatusBar />
	<Header />
	<div class="container absolute isolate p-4">
		<button class="search">
			<font-awesome-icon icon="magnifying-glass" />
			<p>Search</p>
		</button>

		<div class="rowTop absolute grid grid-cols-2 gap-4">
			<div class="projectDiv" v-for="project in projects" :key="project.id">
				<h4 class="m-0 gap-4 text-sm font-normal">{{ project.customer }}</h4>
				<div class="projectNames font-semibold">
					<span>{{ project.title }}</span>
				</div>
				<p class="bottomText">{{ project.uploaded }}</p>
			</div>
		</div>
	</div>
	<Btn />
	<MainNav />
</template>

<script lang="ts">
import StatusBar from './components/StatusBar.vue';
import Header from './components/Header.vue';
import Btn from './components/Btn.vue';
import MainNav from './components/MainNav.vue';

export default {
	name: 'App',

	components: { StatusBar, Header, Btn, MainNav },
	data() {
		return { projects: [] };
	},
	mounted() {
		fetch('http://localhost:5000/projects')
			.then((res) => res.json())
			.then((data) => (this.projects = data))
			.catch((err) => console.log(err.message));
	}
};
</script>
<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	background-color: rgba(237, 240, 243, 1);
	border-radius: 16px;
	height: 812px;
	margin: 50px auto;
	width: 375px;
	top: -723px;

	left: -356px;
}

.container {
	height: 612px;
	width: 375px;
	top: 217px;
	/* box-sizing: border-box; */
}
.container button {
	display: flex;
	height: 36px;
	width: 100px;
	border-radius: 28px;
	border: 1px solid rgba(0, 13, 26, 0.06);
	background-color: rgba(237, 240, 243, 1);
}

.search {
	color: #0055ff;
	font-size: 14px;
	font-family: 'Inter';
	display: flex;
	justify-content: center;
	align-items: center;
	text-align: center;
	font-weight: 600;
	line-height: 20px;
}

.search p {
	padding-left: 4px;
	font-style: normal;
}
.rowTop {
	width: 343px;
	height: 193px;
	top: 68px;
}

.projectDiv {
	width: 163.5px;
	height: 193px;
	background: #ffffff;
	border-radius: 16px;
	box-shadow: 0px 0px 0px 1px rgba(0, 0, 0, 0.03), 0px 1px 4px rgba(0, 0, 0, 0.05);
	padding: 16px;
	gap: 4px;
}

.projectDiv h4 {
	width: 131px;
	font-family: 'Inter';
	color: rgba(0, 0, 0, 0.7);
	font-variation-settings: 'slnt' 0;
	line-height: 20px;
}

.projectNames {
	height: 117px;
	width: 131px;
}

.projectNames span {
	font-size: 16px;
	font-family: 'Inter';
	font-style: normal;
	gap: 4px;
	line-height: 20px;
}

.bottomText {
	font-size: 12px;
	font-weight: 400;
	font-family: 'Inter';
	font-style: normal;
	line-height: 16px;
	color: rgba(0, 0, 0, 0.5);
	padding-top: 6px;
	font-variation-settings: 'slnt' 0;
}
</style>
