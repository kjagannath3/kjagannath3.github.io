<script lang="ts">
    export let title: string;
    export let description: string;
    export let isOpen: boolean;
</script>

<accordionItem>
    <span>
        <h1 class="">{title}</h1>
    </span>
    {#if isOpen}
        <span>
            <p class="">{description}</p>
        </span>
    {/if}
</accordionItem>
