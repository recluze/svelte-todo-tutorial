<!-- Add form at bottom -->
<div class="app-form">
    <input placeholder="Add Todo.." type="text" class="input-text" name="" />
    <button class="btn fa-solid fa-plus" />
</div>

<style>
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
</style>
