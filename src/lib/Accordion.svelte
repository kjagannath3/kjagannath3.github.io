<script lang="ts">
    import CustomAccordionItem from "./CustomAccordionItem.svelte";

    interface IAccordionItem {
        title: string;
        description: string;
        isOpen: boolean;
    }
    let accordionItemsList: IAccordionItem[] = [
        {
            title: "First Item",
            description: "Description for first item",
            isOpen: true,
        },
        {
            title: "Second Item",
            description: "Description for second item",
            isOpen: true,
        },
    ];
</script>

<accordion class="flex place-items-center mt-20 w-4/5 border">
    {#each accordionItemsList as item}
        <CustomAccordionItem
            title={item.title}
            description={item.description}
            isOpen={item.isOpen}
        />
    {/each}
</accordion>

