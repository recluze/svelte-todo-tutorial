<script>
    import { createEventDispatcher } from "svelte";

    import Todo from "./Todo.svelte";

    export let todos;

    const dispatch = createEventDispatcher();
    function forward(event) {
        console.log("Forwarding message", event.detail);
        dispatch("completed", event.detail);
    }
</script>

<!-- List of actual todos -->
<div class="app-body">
    <ul>
        {#each todos as todo}
            <Todo
                itemId={todo.id}
                itemText={todo.text}
                completed={todo.completed}
                on:completed={forward}
            />
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
