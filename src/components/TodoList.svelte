<script>
    import Todo from "./Todo.svelte";

    export let todos; 
</script>

<!-- List of actual todos -->
<div class="app-body">
    <ul>
        {#each todos as todo}
            <Todo itemText ={todo.text} completed = {todo.completed} />
        {/each}
    </ul>
</div>

<style>
    ul {
        border-top: 1px solid rgb(121, 121, 121);
        padding-top: 10px;
        list-style-type: none;
        padding-left: 0px;
    }

    .app-body {
        flex-grow: 1;
        max-height: 600px;
        overflow-x: hidden;
    }
</style>
