<script>
    // components
    import CodeMirror from "svelte-codemirror-editor";
    import Terminal from "$lib/comps/terminal.svelte"
    import Header from "$lib/comps/editor_top.svelte"
    import BlobHeader from "$lib/comps/blob.svelte"

    // content
    import { python } from "@codemirror/lang-python";
    import { barf } from 'thememirror';

    // states
    import { content } from '$lib/states/content.svelte.js'
    import { tools } from "$lib/states/tools.svelte.js"
</script>

<div class="main">
    <Header { content }/>
    <div class="tools">
        {#if tools.terminal}
            <Terminal />
        {/if}
        {#if tools.blob}
            <BlobHeader url={tools.blob_url} />
        {/if}
    </div>
    <CodeMirror bind:value={content.value}  lang={python()} extensions={[barf]} styles={{
        "&": {
            height: tools.blob ? "83vh" : "88vh",
        },
    }}/>
</div>