<script>
  import MenuItem from './MenuItem.svelte';
  const items = ['Home', 'Works', 'About', 'Contact'];

  let { active } = $props();
</script>

<ul class={`${active ? 'active' : ''}`}>
  {#each items as item (item)}
    <MenuItem {item} {active} />
  {/each}
</ul>

<style lang="scss">
  ul {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
    width: 0;
    transition: width 0.6s linear;
    &.active {
      width: 100%;
    }
  }
</style>
