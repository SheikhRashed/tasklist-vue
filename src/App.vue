<template lang="">
	<div>
		<header>
			<h1>Vue Course Goals</h1>
		</header>
		<section id="user-goals">
			<h2>My course goals</h2>
			<input type="text" />
			<button>Add Goal</button>
			<p>No goals have been added yet - please start adding some!</p>
			<ul>
				<li>Goal</li>
			</ul>
		</section>
	</div>
</template>
<script>
	export default {
		name: 'App',
		data() {
			return {
				goals: [],
			}
		},
	}
</script>
<style lang=""></style>
