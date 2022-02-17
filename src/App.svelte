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

<style lang="scss">
nav {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 3em;

  & :global(a) {
    margin: 0 1em;
  }
}

main {
  max-width: 640px;
  margin: 0 auto;  
}
</style>