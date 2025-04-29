<script>
    let { content } = $props()
</script>

<div class="main-top">
    <p>view</p>
    <p class="right">wc: {content.value.split(" ").length} | lc: {content.value.split('\n').length}</p>
</div>

<style>
    .main-top {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
    }
    
    .right {
        color: #c4c4c4;
    }
</style>