<script context="module" lang="ts">
    /**
        each .svelte is actually sort of a javascript/typescript file in disguise.
        context="module" indicates functions and exports declared here delongs to the actual script.
        Here we just use this block to export typescript types for better auto-complete.
    */
    export interface NavItem {
        name: string;
        target: string; //url to navigate to on click
    }
</script>

<script lang="ts">
    import { afterNavigate } from "$app/navigation";

    // lang = 'ts' indicate this component opts in on typescript

    export let navItems: NavItem[] = [];

    let currentRoute = ""; // when this changes, the match anchor tag will update in the #each block.

    afterNavigate((nav) => {
        // when a page is loaded, we can check the url from nav here.
        currentRoute = nav.to?.route.id!;
    });
</script>

<div class="navWrapper">
    <nav>
        <!-- the navWrapper exists so nav could be centered, while still directly containing the nav items. -->
        {#each navItems as item}
            <!-- SvelteKit prefers to use <a>, anchor tags to navigate between pages. (although im personally a goto() abuser) -->
            <a href={item.target} class="navItem" class:selected={item.target === currentRoute}>
                {item.name}
            </a>
        {/each}
    </nav>
</div>

<style>
    .navWrapper {
        /* We want the nav to stay on top regardless of scroll, so position is fixed. */
        position: fixed;
        left: 0;
        top: 2rem;

        width: 100dvw;

        display: flex;
        flex-direction: row;
        justify-content: center;
    }

    a.navItem {
        background-color: var(--bg0); /* re using background color just to create contrast */

        /* make the anchor tag not look like links */
        color: black;
        text-decoration: none;

        padding: 1rem 1rem;

        border-radius: 10px;
        border: 2px solid var(--fg0);

        transition: border-color 0.3s ease-out;
    }

    a.navItem.selected {
        border-color: var(--focus); /* make the active page have it's button highlighted */
    }

    nav {
        width: fit-content; /* prevents nav from fillter the entire available width */
        height: 3rem;

        background-color: var(--bg1);

        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        gap: 1.25rem;

        border: 2px solid black;
        border-radius: 10px;

        padding: 1rem 4rem;
    }
</style>
