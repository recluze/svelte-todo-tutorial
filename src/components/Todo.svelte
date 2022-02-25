<script>
    import { createEventDispatcher } from "svelte";

    export let itemId;
    export let itemText;
    export let completed;

    const dispatch = createEventDispatcher();

    function clickComplete(id) {
        console.log("Clicked complete!", id);
        dispatch("completed", {
            id: id,
        });
    }

    function clickDelete(id) {
        console.log("Clicked delete!", id);
        dispatch("deleted", {
            id: id,
        });
    }
</script>

<li class="todo-list list-item-view {completed ? 'completed' : ''}">
    <span>
        <button
            class="btn btn-done fa-solid {completed
                ? 'fa-square-check'
                : 'fa-square'}"
            on:click={() => clickComplete(itemId)}
        />
        <span>{itemText}</span>
    </span>
    <button
        class="btn btn-delete fa-solid fa-trash"
        on:click={() => clickDelete(itemId)}
    />
</li>

<style>
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
