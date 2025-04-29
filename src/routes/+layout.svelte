<script>
    let { children } = $props()

    // states
    import { tools } from "$lib/states/tools.svelte.js"
    import { content } from "$lib/states/content.svelte.js";
</script>

<nav>
    <div class="right">
        <p>pwep</p>
    </div>
    <div class="left">
        <a href="/about">about</a>
        <a href="/">load</a>
        <a href="/help">helpkit</a>
        <a href={null} onclick={() => {
            const blob_class = new Blob([content.value], {type: "text/x-python"})
            tools.blob_url = URL.createObjectURL(blob_class)
            tools.blob = true
        }} class="btn">blob</a>
        <a href={null} onclick={() => {
            if (tools.terminal) {
                tools.terminal_c++
            } else {
                tools.terminal = true;
            }
        }} class="btn green">run</a>
    </div>
</nav>

<style>
    nav {
        display: flex;
        justify-content: space-between;
        padding-left: 20px;
        padding-right: 20px;
        padding-top: 5px;
        padding-bottom: 5px;
        background-color: #0b0b0b;
        border-bottom: solid 1.8px #4e4e4e63;
        color: #ebebeb;
    }
</style>

{@render children()}