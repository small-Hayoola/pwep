<div class="main">
    <p>/pweb helpkit</p>
    <div>
        <p>pweb has three main functionalities: </p>
        <p class="btm top">- edit a python file</p>
        <p class="btm">- create a python file/blob and download it</p>
        <p class="btm">- run a python file/blob and execute a python shell emulator completly on the browser</p>

        <p class="top-x">to edit a python file, start typing in the box provided on the main area or click <a href="/">load</a> on the top</p>
        <p class="btm top">- note that the text will be lost after a refresh unless you download a blob</p>
        <p class="btm">- additionally you will be able to change the file name via the blob function    </p>

        <p class="top-x">each time you press the <a href={null} class="btn">blob</a> button on the top the program will create a file with the text that you have written on the editor</p>
        <p class="btm top">- in order to add the content on the text to the blob, you have to manually click the blob function again</p>
        <p class="btm">- this prevents unnecesary state changes on events that are fired everytime the text changes, optimizing the program</p>
        <p class="btm">- it is not recomended but you can toggle this feature off in the <a href='/'>config</a> file</p>

        <p class="top-x">the <a class="btn green" href="/">run</a> button will launch a <a href="/">pyscript</a> emulation program</p>
        <p class="btm top">- note that the content that is launched through to pyscript is non dependant on your blob content (no need to update anything)</p>
        <p class="btm">- pyscript is a framework built wit pyodide a python to webassembly interpreter that runs on the web via wasm itself</p>
    </div>
    
</div>

<style>
    .main {
        margin-top: 40px;
    }
    .main div {
        margin-top: 17px;
        font-size: 14px;
    }
</style>