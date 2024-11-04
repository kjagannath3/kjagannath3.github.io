<script lang="ts">
    export let title: string = "Insert title here";
    export let blurb: string =
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eufugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.";
    export let visible: boolean = false;
</script>

<accordionElement class="transition-all duration-200 grid place-items-center my-10 w-3/5  text-center ">
    <button on:click= {() => {visible = !visible}} class="transition-all duration-100 hover:border hover:rounded-full hover:bg-gray-50 hover:text-slate-600 self-center font-bold text-3xl  bg-slate-600 text-gray-50 w-full ">{title}</button>

    <button class="transition-all duration-100 bg-slate-50 overflow-hidden {visible ? 'h-full':'h-0'}">{blurb}</button>
</accordionElement>
