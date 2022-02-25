<script>
	import Header from "./components/Header.svelte";
	import TodoList from "./components/TodoList.svelte";
	import Form from "./components/Form.svelte";

	let todos = [
		{ id: 1, text: "First", completed: false },
		{ id: 2, text: "Second", completed: true },
		{ id: 3, text: "Third", completed: true },
	];
</script>

<div id="app-container" class="app-container">
	<Header />

	<TodoList todos = { todos } />

	<Form />
</div>

<style>
	.app-container {
		width: 400px;
		min-height: 500px;
		background-color: #282c34;
		box-shadow: 0 20px 80px rgba(0, 0, 0, 0.6);
		background: radial-gradient(
			circle,
			#282c34 0%,
			rgba(40, 48, 56, 1) 100%
		);
		position: relative;
		border-radius: 1em;
		padding: 20px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
</style>
