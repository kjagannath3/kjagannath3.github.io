<script lang="ts">
    import { fade, slide } from "svelte/transition";

    export let title: string = "ALERT: Add some text here";
    export let description: string = "No Description Provided";
    let hover: boolean = false;
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<interestElement
    class="transition-all duration-400 px-10 pt-2 text-2xl {hover? 'h-full' : 'h-2/3'} w-52 font-semibold text-indigo-400 border rounded mx-16 place-items-center text-center"
    aria-label="Hoverable element"
    on:mouseenter={() => (hover = true)}
    on:mouseleave={() => (hover = false)}
>
    <h1 class="">{title}</h1>
    <p class="transition-all duration-75 text-sm text-black {hover ? 'opacity-100':'opacity-0'}">{description}</p>
</interestElement>
