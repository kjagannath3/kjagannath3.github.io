<script lang="ts">
    export let title: string = "Default title";
    export let imagePath: string | null = null;
    let hover: boolean = false;
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<!-- svelte-ignore a11y-click-events-have-key-events -->
<interestElement class="p-10 m-16 w-56 border border-black rounded-l">
    <span>

    <h1 class="font-bold text-2xl">{title}</h1>



    </span>
    {#if imagePath}
        <img src={imagePath} alt={title}>
    {:else}
        <h1 class="text-red-500"> Error: No image path provided </h1>
    {/if}

</interestElement>
