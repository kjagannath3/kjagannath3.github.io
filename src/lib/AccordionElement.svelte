<script lang="ts">
    let title: string = "Insert title here";
    let blurb: string =
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eufugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.";

</script>

<accordionElement class="grid place-items-center my-28 w-3/5  text-center border">
    <button class="self-center font-bold text-3xl border  bg-slate-200 w-full ">{title}</button>

    <button class="bg-slate-50 overflow-hidden h-full">{blurb}</button>
</accordionElement>
