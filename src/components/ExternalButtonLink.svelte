<script>
  export let title;
  export let type;
  export let href;
</script>

<style>
  .button-link {
    border: none;
    outline: none;
    background: transparent;
    font-size: 16px;
    font-weight: 600;
    text-decoration: none;
  }
  .primary {
    background: var(--primary);
    color: #fefefe;
    padding: 15px;
    cursor: pointer;
    transition: all 0.5s ease;
  }
  .primary:hover {
    background: var(--text);
  }
</style>

<a {href} tinro-ignore class="button-link {type}">{title}</a>
