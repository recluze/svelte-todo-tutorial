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
