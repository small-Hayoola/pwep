<script>
    import { content } from "$lib/states/content.svelte.js";
    import { tools } from "$lib/states/tools.svelte";
    let code = content.value

    $effect(() => {
        code = content.value
    })
</script>

<div class="terminal">
    <div class="terminal-close">
        <p>terminal</p>
        <a class="btn close" href={null} onclick={() => tools.terminal = false}>close</a>
    </div>
    {#key tools.terminal_c}
        {@html '<py-script type="py" terminal worker>' + code + '</py-script>'}
    {/key}
</div>

<style>
    .terminal {
        z-index: 9;
        position: absolute;
        top: 50px;
        right: 50px;
        border: 1px #565656 solid;
        background-color: #191a19;
    }

    .terminal-close {
        border-bottom: 1px #565656 solid;
        display: flex;
        justify-content: space-between;
        padding-left: 8px;
        padding-right: 8px;
        padding-top: 2px;
        padding-bottom: 2px;
    }

    a {
        font-size: 12px;
    }

    .terminal-close p {
        font-size: 12px;
    }
</style>