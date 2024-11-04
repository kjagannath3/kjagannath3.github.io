<script lang="ts">
    export let title: string = "ALERT: Add some text here";
    export let description: string = "No Description Provided";
    let hover: boolean = false;
    export let blurb: string = "Insert Blurb here";
    let modalVisibility: boolean = true;
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<!-- svelte-ignore a11y-click-events-have-key-events -->
<interestElement
    class="transition-all duration-400  pt-5 text-2xl {hover
        ? 'h-auto'
        : 'h-2/5'}  w-52 font-semibold text-slate-500 border rounded mx-16 place-items-center text-center"
    aria-label="Hoverable element"
    on:mouseenter={() => (hover = true)}
    on:mouseleave={() => (hover = false)}
    on:click={() => {
        modalVisibility = !modalVisibility;
    }}
>
    <h1 class="">{title}</h1>
    <p
        class="p-0 transition-all duration-200 text-sm text-black {hover
            ? 'opacity-100'
            : 'opacity-0'}"
    >
        {description}
    </p>
</interestElement>
