<script lang="ts">
    import AccordionElement from "./AccordionElement.svelte";
    import { onMount } from "svelte";
    let currentVisibleTitle: string | null = null;
    
    interface IAccordionElement {
        title: string;
        blurb: string;
        imgPath?: string;  // Optional because projects don't have images
        visible?: boolean;  // Optional for accordion state
    }
    export let accordionElements: Array<IAccordionElement> = [
        {
            title: "This is a default title 1",
            blurb: "This is a default blurb 1",
        },
        {
            title: "This is a default title 2",
            blurb: "This is a default blurb 2",
        },
        {
            title: "This is a default title 3",
            blurb: "This is a default blurb 3",
        },
        {
            title: "This is a default title 4",
            blurb: "This is a default blurb 4",
        },
    ];

</script>

<accordion class="flex  mt-20 w-4/5 border min-h-[300px]">
    <mainAccordion
        class="grid place-items-center w-full overflow-y-auto min-h-[300px]"
    >
        {#each accordionElements as child (child.title)}
            <AccordionElement
                title={child.title}
                blurb={child.blurb}
                visible={child.visible}
                imgPath={child.imgPath}
            />
        {/each}
    </mainAccordion>
</accordion>
