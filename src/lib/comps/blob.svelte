<script>
    // states
    import { content } from "$lib/states/content.svelte.js";
    import { tools } from "$lib/states/tools.svelte.js";
    let blob_val = $state("main.py")

    // content
    const { url } = $props()
</script>

<div class="blob-main">
    <div class="blob-right">
        <img width="22px" src="/py.png" alt="py_file"/>
        <input id='file' bind:value={blob_val} />
    </div>
    <div>
        <a href={null} onclick={() => tools.blob = false} class="btn close">close</a>
        <a href={url} download={blob_val} class="btn trans">download</a>
    </div>
</div>

<style>
    .blob-main {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #1d1d1d;
        padding-top: 4px;
        padding-bottom: 4px;
        padding-right: 8px;
        padding-left: 8px;
        border-radius: 6px;
        margin-bottom: 8px;
    }

    .blob-right {
        display: flex;
        align-items: center;
    }

    .blob-right input {
        border: none;
        background-color: #00000000;
        color: #d8d6d6;
        outline: none;
        margin-left: 10px;
        font-size: 14px;
    }
</style>