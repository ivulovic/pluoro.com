<script>
  export let src;
  export let href;
  export let title;
</script>

<style>
  .card {
    text-decoration: none;
    color: var(--text);
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .card .image {
    height: 150px;
    width: 100%;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
  }
  .card h3 {
    display: block;
    width: 100%;
    text-align: center;
    margin: 10px 0px 0px 0px;
  }
</style>

<a {href} tinro-ignore class="card">
  <div class="image" style="background{`-image: url(${src});`}" />
  <h3>{title}</h3>
</a>
