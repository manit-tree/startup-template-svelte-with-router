# Startup Template for Svelte + Router + Vite

This template should help get you started developing with Svelte in Vite quickly. It comes pre configured with SCSS and Svelte Routing (using svelte-navigator package).

## Usages

```
git clone https://github.com/manit-tree/startup-template-svelte-with-router.git
cd startup-template-svelte-with-router
npm i
npm run dev
```

## Basic Route

```
# ./src/App.svelte

<script>
	import { Router, Link, Route } from "svelte-navigator";
	import Home from "./routes/Home.svelte";
	import About from "./routes/About.svelte";
	import Contact from "./routes/Contact.svelte";
</script>

<Router>
  <nav>
    <Link to="/">Home</Link>
    <Link to="about">About</Link>
    <Link to="contact">Contact</Link>
  </nav>
  <div>
    <main>
       <Route path="/" component={Home} />
       <Route path="about" component={About} />
       <Route path="contact" component="{Contact}" />
    </main>
  </div>
</Router>
```

For more information about how to use svelte-navigator, please visit https://www.npmjs.com/package/svelte-navigator
