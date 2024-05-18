<script lang="ts">
    import { onNavigate } from "$app/navigation";
    import NavBar, { type NavItem } from "$lib/components/NavBar.svelte";
    
    import "../global.css"; // its nice to have a style sheet applied to the entire app, this is one way to do it.

    let navTargets: NavItem[] = [
        {
            name: "Home",
            target: "/",
        },
        {
            name: "Todo",
            target: "/todo",
        },
        {
            name: "About",
            target: "/about",
        },
    ];


</script>

<!-- make the NavBar in layout so that every subpage gets it. -->
<NavBar navItems={navTargets} />

<slot />
