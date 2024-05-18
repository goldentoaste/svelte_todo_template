<script lang="ts">
    import List from "$lib/components/TodoList.svelte";
    import type { TodoItem } from "$lib/globals";

    let todoItems: TodoItem[] = [
        {
            id:"1",
            message: "Finish workshop website",
            done: false,
        },
        {id:"2",
            message: "Deploy api",
            done: false,
        },
        {id:"3",
            message: "eat dinner",
            done: true,
        },
    ];
</script>

<h1>My Todo List 📝</h1>

<!-- Import and put the TodoList Component here, and give it the list of todoItems. -->

<style>

</style>
