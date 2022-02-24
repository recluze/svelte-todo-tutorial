<script>
	import Header from './components/Header.svelte'
	import Form from './components/Form.svelte'
</script>

<div id="app-container" class="app-container">
	
	<Header /> 

	<!-- List of actual todos -->
	<div class="app-body">
		<ul>
			<li class="todo-list list-item-view">
				<span>
					<button class="btn btn-done fa-solid fa-square" />
					<span>First Todo</span>
				</span>
				<button class="btn btn-delete fa-solid fa-trash" />
			</li>

			<li class="todo-list list-item-view completed">
				<span>
					<button class="btn btn-done fa-solid fa-square-check" />
					<span>Second Todo</span>
				</span>
				<button class="btn btn-delete fa-solid fa-trash" />
			</li>

			
		</ul>
	</div>


	<Form /> 
	
</div>




<style>
	ul {
		list-style-type: none;
		-webkit-padding-start: 0;
		padding-left: 0px;
	}

	.btn {
		color: inherit;
		cursor: pointer;
		font-size: 15px;
		padding: 10px 12px;
		border-radius: 2em;
		background: none;
		border: 0px solid;
		transition: 250ms ease-out;
	}

	.btn:hover {
		background: #1d2025;
	}

	.btn:focus {
		outline: none;
	}

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

	

	.app-body {
		flex-grow: 1;
		max-height: 600px;
		overflow-x: hidden;
	}

	.todo-list:first-of-type {
		border-top: 1px solid rgb(121, 121, 121);
		padding-top: 10px;
	}

	.list-item-view {
		padding-top: 5px;
		padding-bottom: 0px;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	

	.completed {
		color: #6a6f75;
		opacity: 0.5;
	}
</style>
