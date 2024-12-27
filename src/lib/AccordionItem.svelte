<script lang="ts">
    let title: string | null = "Default Title";
    let description: string | null = "Default description";
    let isOpen: boolean = false;
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
