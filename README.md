# pwep

pwep is a simple integrated development environment for  single file python programming on the web created with a web assembly python shell emulator via ``pyscript``, ``code mirror`` (code editor) and bundled with python file/blob creation written with ``svelte`` and ``sveltekit``.

![screenshot](./screenshot.png)

### usage
pwep is deployed via a vercel free automatic plan on [here](https://pwep-ashen.vercel.app/). a help page has been integrated in the app on the ``helpkit`` page or [here](https://pwep-ashen.vercel.app/help) from the ``/help`` route.

> note that the free vercel plan limits web workers and svelte render time therefore pyscript (web python shell emulation tool) might run slower compared to a local build. running the project locally on dev environment or building it might lead to better results

### development

once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
# for installing dependencies
npm install

npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

### building

to create a production version of pweb:

```bash
git clone https://github.com/small-Hayoola/pwep
cd pweb
npm install
npm run build
```

you can preview the production build with `npm run preview`.

> to deploy pweb locally, you may need to install an [adapter](https://svelte.dev/docs/kit/adapters) for your target environment.
