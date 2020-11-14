<script>
  export let url;
  export let name;
  export let selected;
</script>

<style>
  li {
    list-style: none;
  }
  li a {
    text-decoration: none;
    transition: 150ms ease;
  }
  .unselected a {
    color: black;
    font-size: 16px;
  }
  .selected a {
    color: blue;
    font-size: 22px;
    font-weight: bold;
  }
</style>

<li class={selected ? 'selected' : 'unselected'}><a href={url}> {name} </a></li>
