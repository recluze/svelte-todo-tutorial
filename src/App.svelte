<script>
	import Header from './components/Header.svelte'
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
				<!-- <div class="list-item-view"> -->
				<span>
					<button class="btn btn-done"
						><i class="fa-solid fa-check-square" /></button
					>
					<span>First Todo</span>
				</span>
				<button class="btn btn-delete fa-solid fa-trash" />
				<!-- </div> -->
			</li>
		</ul>
	</div>

	<!-- Add form at bottom -->
	<div class="app-form">
		<input
			placeholder="Add Todo.."
			type="text"
			class="input-text"
			name=""
		/>
		<button class="btn fa-solid fa-plus" />
	</div>
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

	.btn-delete {
		color: #666;
		font-size: 0.7em;
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

	.app-form {
		margin-bottom: 10px;
		display: flex;
		justify-content: center;
	}

	.input-text {
		height: 40px;
		background: #282c34;
		font-size: 15px;
		border: 1px solid #a2a8ad;
		color: #dce4ec;
		width: 100%;
		margin-right: 15px;
		border-radius: 2em;
		padding: 5px 10px;
		transition: border 250ms ease-out;
	}

	.input-text:focus {
		border: 1px solid #ffffff;
		background: #1d2025;
		outline: none;
		color: #dce4ec;
	}

	::placeholder {
		opacity: 0.3;
	}

	.completed {
		color: #6a6f75;
		opacity: 0.5;
	}
</style>
