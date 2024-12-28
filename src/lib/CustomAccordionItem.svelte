<script lang="ts">
    export let title: string;
    export let description: string;
    export let isOpen: boolean;
    export let setIsOpen = () => {
        isOpen = !isOpen;
    };
</script>

<accordionItem>
    <span>
        <h1 class="">{title}</h1>
        {#if isOpen}
            <img src="minusicon.png" on:click={setIsOpen} alt="collapse" />
        {:else}
            <img src="plusicon.png" on:click={setIsOpen} alt="collaps" />
        {/if}
    </span>
    {#if isOpen}
        <span>
            <p class="">{description}</p>
        </span>
    {/if}
</accordionItem>
