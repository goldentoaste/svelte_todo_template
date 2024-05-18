<script lang="ts">


    // TODO declare the variables here. id, done,
    // id is required so we know which to delete later

    // TODO  make a event dispatcher here. call createEventDispatcher()
</script>

<!-- "✔️" : "❌" -->
<!-- The todo item will be really simple, just a span to display message. and a delete button -->

<div class="todoItem">
    <!-- TODO give the item different style depending on 'done' -->
    <!-- TODO add a transition here? for when item is created or deleted. -->

    <span>
        <!-- TODO dispatch a "toggleDone" event here on click -->

        <!-- TODO display the message here. -->
        <!-- display "✔️" or "❌" here depending on one -->
    </span>

    <button class="deleteButton" > 
        <!-- TODO dispatch a "delete" event when clicked. -->
        Delete
    </button>
</div>



<style>
    .todoItem {
        border-radius: 10px;
        border: 2px solid var(--focus);
        padding: 1rem;
        background-color: var(--bg0);

        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .done {
        background-color: var(--green);
    }

    .todoItem:not(.done) {
        /* find .todoItem that isn't .done */
        background-color: var(--red);
    }

    .deleteButton {
        margin-left: 1rem;
        padding: 0.5rem;
        border: 2px solid var(--focus);
        border-radius: 5px;
        background-color: var(--fg1);
    }

    button {
        cursor: pointer;
        transition: all 0.3s ease-out;
    }

    button:hover {
        filter: brightness(1.1);
        background-color: var(--bg0);
    }

    span {
        cursor: pointer;
        user-select: none;
    }
</style>
