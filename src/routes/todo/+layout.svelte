<div class="todoRoot">
    <!-- todoRoot provides styling for the page. -->
    <!-- this 'slot' will be replace by the page -->
    <slot />
</div>

<style>
    .todoRoot {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        gap: 1rem;


        width: 100%;
        height: fit-content;

        padding: 2rem 5rem;

        /* border-box accounts padding in it's size calculation, so that width:100% works with padding. */
        box-sizing: border-box;
    }
</style>
