<script lang="ts">
import AccordionElement from "./AccordionElement.svelte";

	let accordionElements: Array<AccordionElement> = [
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
	let defaultImagePath: string = "defaultImage.png";
</script>

<accordion class="flex w-4/5 mt-20">
	<img src={defaultImagePath} alt="" />
	<mainAccordion class="ml-32">
		<h1>
            This is the accordion
		</h1>

		{#each accordionElements as child(child.title)}
            <AccordionElement title={child.title} blurb={child.blurb} />    
        {/each}
	</mainAccordion>

</accordion>
