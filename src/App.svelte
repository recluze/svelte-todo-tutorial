<script>
	import Header from "./components/Header.svelte";
	import TodoList from "./components/TodoList.svelte";
	import Form from "./components/Form.svelte";

	let todos = [
		{ id: 1, text: "First", completed: false },
		{ id: 2, text: "Second", completed: true },
		{ id: 3, text: "Third", completed: true },
	];

	let remainingTodos;
	let totalTodos;
	let newText;

	$: totalTodos = todos.length;
	$: remainingTodos = todos.reduce((n, todo) => {
		return n + (todo.completed ? 0 : 1);
	}, 0);

	function onCompleted(event) {
		console.log("Received at top", event.detail);
		let updateId = event.detail.id;
		todos.map((todo) => {
			if (todo.id == updateId) todo.completed = !todo.completed;
		});
		// console.log(todos);
		todos = todos; // reactivity triggered by assignment
	}

	function createdTodo(event) {
		console.log("In App created", newText);
		newText = newText.trim();

		if (newText != "") {
			let newId = Math.max(...todos.map((e) => e.id)) + 1;
			todos = [...todos, { id: newId, text: newText, completed: false }];
		}
	}
</script>

<div id="app-container" class="app-container">
	<Header {totalTodos} {remainingTodos} />

	<TodoList {todos} on:completed={onCompleted} />

	<Form on:created={createdTodo} bind:newText />
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
