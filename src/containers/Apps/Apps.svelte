<script>
  import { onMount } from "svelte";
  import request, {
    makeApiUrl,
    makePostReq,
    makeAuthUrl,
  } from "../../utils/request";
  import Card from "../../components/Card.svelte";

  // icons: https://www.iconfinder.com/iconsets/metro-ui-icon-set
  onMount(async () => {
    try {
      const res = await request(makeAuthUrl(`/account/test`), makePostReq());
      const res2 = await request(makeApiUrl(`/app/test`), makePostReq());
    } catch (error) {
      console.log(error);
    }
  });
</script>

<style>
  main {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    grid-row-gap: 40px;
    grid-column-gap: 25px;
    color: var(--text);
    padding-top: 25px;
  }
</style>

<main>
  <div>
    <Card href="/notes" src="/static/apps/notes.png" title="Notes" />
  </div>
  <div>
    <Card href="/blog" src="/static/apps/blog.png" title="Blog" />
  </div>
</main>
