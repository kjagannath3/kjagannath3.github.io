<script lang="ts">
    export let title: string = "Insert title here";
    export let blurb: string =
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent nec ligula eu nisi consequat ultricies vel a urna. Curabitur dapibus, nisl vel varius lacinia, eros enim pellentesque justo, sit amet feugiat eros ligula a urna. Suspendisse potenti. Nulla facilisi. Integer euismod elit vel dictum fermentum. Nam eget nisi auctor, laoreet justo quis, sodales ex. Vivamus vestibulum, lorem nec gravida fermentum, eros ipsum condimentum nulla, non luctus felis mi vel justo. Donec id faucibus est, in venenatis sapien. Fusce malesuada ante ut libero suscipit, a sollicitudin metus gravida. Pellentesque volutpat leo et ex ultrices, nec molestie nisl malesuada.";
    export let visible: boolean = false;
</script>

<accordionElement
    class="transition-all duration-200 grid place-items-center w-3/5 text-center my-1"
>
    <button
        on:click={() => {
            visible = !visible;
        }}
        class="transition-all {visible
            ? 'bg-slate-200 text-slate-600 rounded-full'
            : 'bg-slate-600 text-slate-50 rounded-md'} duration-100 border-4 border-slate-50 hover:border-slate-600 hover:bg-gray-50  hover:text-slate-600 self-center font-bold text-3xl text-gray-50 w-full"
        >{title}</button
    >

    <button
        class="transition-all duration-100 bg-slate-50 overflow-hidden {visible
            ? 'h-full'
            : 'h-0'}">{blurb}</button
    >
</accordionElement>
