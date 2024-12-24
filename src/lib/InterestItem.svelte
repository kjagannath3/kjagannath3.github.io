<script lang="ts">
    export let title: string = "Default title";
    export let description: string = "Default Description";
    let hover: boolean = false;
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<!-- svelte-ignore a11y-click-events-have-key-events -->
<interestElement class="p-10 m-16 w-56 border border-black rounded-l">
    <h1 class="font-bold text-2xl">{title}</h1>
</interestElement>
