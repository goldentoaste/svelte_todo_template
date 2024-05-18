<script lang="ts">
    // include the uuid library here to be less confusing, maybe.
    import { v4 as uuid4 } from "uuid";


    // TODO delcare a list of todos and export it.

    // TODO declare a variables for the input field on bind onto.



    // TODO write a function to toggle item status by index

    // TODO write a func to delete item by index

    // TODO func to add new todo item. (use the uuid4 func to gen id)

</script>


<!-- TODO add item to list on submit -->
<form >
    <!-- bind value to a variable to be used during add -->
    <input type="text"  />
</form>

<div class="listContainer">
    <!-- TODO write a #each to render, give it index and key to be efficient. -->

    <!-- TODO create the TodoListItems inside here -->
    <!-- give it the todo's information -->
    
    <!--  TODO handle toggleDone, handle delete events.  -->

</div>

<style>
    .listContainer {
        padding: 1rem;
        border-radius: 10px;
        border: 2px solid var(--focus);

        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    input {
        margin: 1rem;
        /* reduce by 3 rem due to margin and padding on both sides */
        width: calc(100% - 3rem);

        border: 2px solid var(--focus);
        border-radius: 5px;

        font-size: x-large;
        padding: 0.5rem;
    }
</style>
