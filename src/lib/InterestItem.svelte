<script lang="ts">
    export let title: string = "ALERT: Add some text here";
    export let description: string = "No Description Provided";
    let hover: boolean = false;
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<interestElement
    class="px-10 py-20 text-3xl font-semibold text-indigo-400"
    aria-label="Hoverable element"
    on:mouseenter={() => (hover = true)}
    on:mouseleave={() => (hover = false)}
>
    {#if !hover}
        <h1>{title}</h1>
    {/if}
    {#if hover}
        <p>{description}</p>
    {/if}
</interestElement>
