<script>
  export let subtitle;
  export let title;
</script>

<style>
  main {
    text-align: center;
    font-weight: 500;
  }
  .subtitle {
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 0.03rem;
    color: var(--primary);
  }
  .title {
    font-size: 32px;
    color: var(--text);
    margin: 15px 0px 10px 0px;
    font-weight: 600;
  }
  .divider {
    display: inline-block;
    height: 2px;
    width: 100px;
    background: var(--primary);
  }
</style>

<main>
  <p class="subtitle">{subtitle}</p>
  <p class="title">{title}</p>
  <div class="divider" />
</main>
