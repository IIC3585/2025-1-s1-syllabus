# Diseño Avanzado de Aplicaciones Web

Estos recursos son complementarios. Las clases están subidas en Canvas.

## Recursos generales

- [Evan You - Frontend tooling, past and future](https://www.youtube.com/watch?v=5mn3EpWCcJs&t=16343s)
- CSS:
  - Nueva propuesta de layouts en CSS: [item-flow](https://webkit.org/blog/16587/item-flow-part-1-a-new-unified-concept-for-layout/)
  - [Pensando en StyleX](https://stylexjs.com/docs/learn/thinking-in-stylex/) (sistema que usa META)
- Temas IAs:
  - [Artificial Analysis](https://artificialanalysis.ai) para conocer diferentes modelos y sus capacidades
  - “ChatGPTs” para apps web: [bolt.new](https://bolt.new/), [v0.dev](https://v0.dev), [lovable](https://lovable.dev/), etc
  - Editores con IA para probar: [Cursor](https://cursor.com), [Copilot](https://github.com/features/copilot), [Zed](https://zed.dev/), [Windsurf](https://codeium.com/windsurf), [Trae](https://www.trae.ai/)
  - [Model Context Protocol](https://modelcontextprotocol.io/introduction) y su documentación en [Cursor](https://docs.cursor.com/context/model-context-protocol)
  - Como el [CEO de builder.io (IA + Figma y CMS) usa Cursor](https://www.linkedin.com/video/live/urn:li:ugcPost:7303840329999208448/)
  - Casos de usos de [Convex con MCP](https://stack.convex.dev/convex-mcp-server)

## Recursos recomendados a revisar para las tareas

Las tareas son públicas, les recomendamos revisar repositorios de semestres pasados.

> [!TIP]
>
> Deben tener **todo** el material que usen en sus repositorios, y subido los demos para que puedan ser probados.
>
> Consideren que **más de la mitad del trabajo se califica en ir “más allá”** (calidad, elegancia, mantenibilidad, documentación), poder explicar bien el diseño e implementación, y mostrar aspectos interesantes relacionados.

### Tarea 1: JavaScript Funcional

> Deploy recomendado: [Vite vanilla-ts](https://vite.dev/guide/#scaffolding-your-first-vite-project) y [GitHub Pages](https://vite.dev/guide/static-deploy.html#github-pages). Si quieren correrlo en el terminal, [Bun](https://bun.sh/).

La charla [Functional Programming Design Patterns](https://fsharpforfunandprofit.com/fppatterns/) (link a [YouTube](https://youtu.be/srQt1NAHYC0)), la charla [Functional programming patterns for the non-mathematician](https://youtu.be/AvgwKjTPMmM), y el post [Lazy, composable, and modular JavaScript](https://codewords.recurse.com/issues/four/lazy-composable-and-modular-javascript).

Ejemplos de [Left y Right](https://effect.website/play/#d7103f0ecade), y del [patrón Effect](https://effect.website/play/#d4de9a1af80b) para el manejo de errores.

[Effect](https://effect.website/) es una librería moderna que usa varios patrones funcionales, que ha ganado tracción considerable.
La librería [`fp-ts`](https://github.com/gcanti/fp-ts), enfocada principalmente en primitivos de estilo funcional, se [sumó a Effect](https://dev.to/effect/a-bright-future-for-effect-455m).

[Gleam](https://gleam.run/) es un lenguaje funcional que corre en [Erlang](https://www.erlang.org/).
Es un lenguaje funcional inspirado en [Elixir](https://elixir-lang.org/), y permite ser compilado a JavaScript.

[RxJS](https://rxjs.dev/), librería enfocada al manejo de eventos, que fue bien usado en [Angular](https://angular.dev/ecosystem/rxjs-interop/output-interop).
[Loadash](https://lodash.com/) es una de las primeras grandes librerías de JS que incluía [patrones funcionales](https://github.com/lodash/lodash/wiki/fp-guide).

Este articulo de SO que habla de [Reactive Programing](https://stackoverflow.com/q/1028250), que es tangencial a la programación funcional, y tiene ideas que ha tomado frameworks como Svelte.

### Tarea 2: Web Assembly y PWAs

> Deploy recomendado: [Vite vanilla-ts](https://vite.dev/guide/#scaffolding-your-first-vite-project) (o un framework) y [GitHub Pages](https://vite.dev/guide/static-deploy.html#github-pages).
>
> Notificaciones: [Firebase Cloud Messaging](https://firebase.google.com/docs/cloud-messaging).
>
> WASM: Rust con [wasm-pack](https://github.com/rustwasm/wasm-pack)

#### Rust y WASM

- La [guia de `wasm-bindgen`](https://rustwasm.github.io/docs/wasm-bindgen/) (lo que se encarga del build) y la de [`wasm-pack`](https://rustwasm.github.io/wasm-pack/book/introduction) (lo que se encarga de empaquetado)
- Correrlo en vite con [`vite-plugin-wasm`](https://github.com/aleclarson/vite-plugin-wasm).
- Tutoriales de [mozilla](https://developer.mozilla.org/en-US/docs/WebAssembly/Guides/Rust_to_Wasm), videos tutoriales rápidos [sin bundler](https://youtu.be/nW71Mlbmxt8) y [con Vite](https://youtu.be/8zDYoprO358).

#### Rust, WASM y procesamiento de imagenes

- La crate [`image`](https://crates.io/crates/image), muy usada para procesamiento de imagenes.
- El [proyecto Photon](https://silvia-odwyer.github.io/photon), editor simple de imagenes en WASM.
- Proyectos más pequeños como [imageproc-website](https://github.com/arthmis/imageproc-website) y [wasm-image](https://github.com/peerigon/wasm-image).

#### WASM Showcase

- [La página de WebAssembly](https://webassembly.org/), especialmente el [FAQ](https://webassembly.org/docs/faq/).
- [WebAssembly proposals](https://webassembly.org/features/). El que se destaca más y que probablemente usen, es un polyfil de [ESModule Integration](https://github.com/WebAssembly/esm-integration).

#### PWA general

- [Documentación de mozilla](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps).
- [Learn PWA](https://web.dev/learn/pwa) y [Explore Progressive Web Apps](https://web.dev/explore/progressive-web-apps) de Google.
- El [listado de campos disponible en el manifest](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Manifest).
- Trabajar con Web Workers: [Workbox](https://developer.chrome.com/docs/workbox) y su fork [Serwist](https://serwist.pages.dev/), que tiene adaptadores a frameworks.

#### PWA Showcase

- [El showcase del proyecto Fugu de Chrome](https://developer.chrome.com/docs/capabilities/fugu-showcase).
- Varios docs de Learn PWA: [Integrarse al sistema operativo](https://web.dev/learn/pwa/os-integration), [App Shortcuts y Splash Screens](https://web.dev/learn/pwa/enhancements), [Diseño de la App](https://web.dev/learn/pwa/app-design).
- [Nueva API propuesta por Apple para notificaciones push declarativas](https://webkit.org/blog/16535/meet-declarative-web-push/). Es buena lectura para entender por qué Apple no le gustó como estaban implementadas las notificaciones en JS.
- [`idb`](https://github.com/jakearchibald/idb), un wraper de IndexedDB muy usado.

#### PWA en frameworks

- [Vite PWA](https://vite-pwa-org.netlify.app/guide/), que se adapta con Workbox con frameworks basados en Vite como SvelteKit y Nuxt.
- [NextJS](https://nextjs.org) con su [configuración del manifest](https://nextjs.org/docs/app/building-your-application/configuring/progressive-web-apps) y junto a [Serwist](https://serwist.pages.dev/docs/next/getting-started).

### Tarea 3: Frameworks Vue y Svelte

> Deploy recomendado: Cloudflare Workers, Vercel, Netlify. Algo que funcione con múltiples proyectos en el mismo repositorio.

#### Vue

- [Tutorial](https://vuejs.org/tutorial)
- [Vue.js: The Documentary](https://youtu.be/OrxmtDw4pVI)

#### Svelte

- [Tutorial](https://svelte.dev/tutorial)
- [Svelte Origins: A JavaScript Documentary](https://youtu.be/kMlkCYL9qo0)
- Rich Harris:
  - [Rethinking reactivity](https://youtu.be/AdNJ3fydeao)
  - [Introduction to Runes](https://youtu.be/RVnxF3j3N8U)

#### Otros

- [Monorepo con Vue y Svelte](https://github.com/IIC3585/2025-1-s1-pnpm-vue-svelte)

### Tarea 4: Web Components

- Frameworks: [Lit](https://lit.dev/), [Stencil](https://stenciljs.com/)
- [Why Web Components](https://designsystem.webstandards.ca.gov/why-web-components/index.html)
- [MicroFrontends](https://micro-frontends.org/), un estilo de arquitectura web que suele usar Web Components.
- [Web components demystified](https://css-tricks.com/web-components-demystified/)
- Ryan Carniato (Solid.js): [Web Components Are Not the Future](https://dev.to/ryansolid/web-components-are-not-the-future-48bh)

### Tarea 5: Frameworks para SSR

#### Astro

- Astro docs: [Why Astro?](https://docs.astro.build/en/concepts/why-astro/)

#### React Server Components

- [“Mind the Gap”](https://youtu.be/zqhE-CepH2g?si=deRmRFm5y64u15VF) de Ryan Florence (creador React Router / Remix)
- Dan Abramov (React):
  - Los [blogs de RSC](https://overreacted.io/)
  - [Data Fetching with React Server Components](https://youtu.be/TQQPAU21ZUw), y por qué Meta llegó a la creación de estos.
- [Making sense of React Server Components](http://joshwcomeau.com/react/server-components/) de Josh Comeau
- Frameworks: [Next.js](https://nextjs.org), [RedwoodSDK](https://rwsdk.com/), [Expo](https://docs.expo.dev/guides/server-components/), [React Router (Remix)](https://remix.run/blog/rsc-preview)

<!-- Añadir conversaciones de diferentes tipos de aplicaciones web -->
