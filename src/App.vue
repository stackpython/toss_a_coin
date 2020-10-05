<template>
	<div class="coin__container">
		<div class="coin" v-for="(coin, index) in status" :key="index">
			<p>{{ coin }}</p>
		</div>
	</div>
	<button @click="toss">Toss</button>
	<button @click="add">Add Coin</button>
	<button @click="remove">Remove Coin</button>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			status: ['H'],
		};
	},
	methods: {
		toss() {
			const hOrT = 'HT';
			// this.status = hOrT[Math.floor(Math.random() * 2)];
			for (let i in this.status) {
				this.status[i] = hOrT[Math.floor(Math.random() * 2)];
			}
		},
		add() {
			this.status.push('H');
		},
		remove() {
			this.status.pop();
		},
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}

.coin {
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: gold;
	width: 3rem;
	height: 3rem;
	border-radius: 1.5rem;
  margin: 0.2rem;
}

.coin p {
	font-weight: bold;
	color: rgb(247, 247, 247);
}

.coin__container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 1rem;
}
</style>
