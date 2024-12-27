<script lang="ts">
    import { AccordionItem } from "./components/ui/accordion";

    interface AccordionItem {
        title: string;
        description: string;
        isOpen?: boolean;
    }
</script>

<accordion class="flex place-items-center mt-20 w-4/5 border">
    <h1>Hello World</h1>
</accordion>
