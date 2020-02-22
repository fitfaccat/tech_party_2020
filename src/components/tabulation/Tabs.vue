<template>
	<div>
		
		<nav class="menu-talks">
			<a
				v-for="(tab, index) in tabs"
				:key="index"
				:href="tab.href"
				@click="selectTab(tab)"
				:class="{ 'is-active': tab.isActive }"
			>
				{{ tab.name }}
			</a>
		</nav>

		<div class="tab-details">
			<slot></slot>
		</div>
	</div>	
</template>

<script>
export default {
	name: 'Tabs',
	data() {
		return {
			tabs: []
		};
	},
	created() {
		this.tabs = this.$children;
	},
	methods: {
		selectTab(selectedTab) {
			this.tabs.forEach(tab => {
				tab.isActive = (tab.name == selectedTab.name);
			});
		}
	}
}
</script>

<style scoped lang="scss">
$tabulation-color: #e5e5e5;

.menu-talks {
	width: 100%;
	height: 9%;
	display: flex;
	justify-content: space-around;

	.is-active {
		background: $tabulation-color;
		box-shadow: none;
	}
	a {
		flex: 1;
		height: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		box-shadow: inset 1px -2px 5px #0E0B16;
		border-left: 2px solid #0E0B16;
		background: #e84c3d;
		color: #0E0B16;
		font-weight: bold;

		&:first-child { border-left: none; }
	}
}
.tab-details {
	height: 90%;
	overflow-y: auto;
	padding: .5rem 1rem;
}
</style>