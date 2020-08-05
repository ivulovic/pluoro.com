<script>
  // import { Route } from "tinro";
  import { getCookie } from "./utils/cookie";
  import Header from "./components/Header.svelte";
  import NotFound from "./containers/NotFound.svelte";
  import Home from "./containers/Home/Home.svelte";

  const isLoggedIn = !!getCookie("TestAuthorization");
  let theme = localStorage.getItem("theme") || "light";
  const onThemeChange = () => {
    const newTheme = theme === "light" ? "dark" : "light";
    localStorage.setItem("theme", newTheme);
    theme = newTheme;
  };
</script>

<style>
  .base {
    margin: 0 8%;
  }
  @media only screen and (max-width: 1024px) {
    .base {
      margin: 0 10px;
    }
  }
  :global(a.active) {
    color: var(--primary) !important;
  }
  :global(*) {
    margin: 0px;
    padding: 0px;
    font-family: sans-serif;
  }
  :global(html),
  :global(body) {
    height: 100%;
  }
  :global(#root) {
    min-height: 100%;
    background-color: var(--background);
  }
  :global(.theme-light) {
    --primary: #d21e2b;
    --text: #333;
    --background: #fff;
    --edge: #f6f6f6;
    --neutral: #9c9999;
  }
  :global(.theme-dark) {
    --primary: #d21e2b;
    --text: #fff;
    --background: #333;
    --edge: #444;
    --neutral: #383636;
  }
</style>

<div id="root" class="theme-{theme}">
  <div class="base">
    <Header {isLoggedIn} on:themeChange={onThemeChange} />
    <Home />
    <!-- <Route>
      <Route path="/">
        <Home />
      </Route>
      <Route fallback>
        <NotFound />
      </Route>
    </Route> -->
  </div>
</div>
