<script lang="ts">
    import { fade } from "svelte/transition";

    export let title: string = "ALERT: Add some text here";
    export let description: string = "No Description Provided";
    let hover: boolean = false;
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<interestElement
    class="px-10 py-2 text-2xl h-52 w-52 font-semibold text-indigo-400 border rounded mx-16 place-items-center text-center"
    aria-label="Hoverable element"
    on:mouseenter={() => (hover = true)}
    on:mouseleave={() => (hover = false)}
>
    <h1 class="">{title}</h1>
    {#if hover}
        <p transition:fade class="text-sm text-black">{description}</p>
    {/if}
</interestElement>
