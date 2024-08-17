<script>
  import Button from './lib/Button.svelte';
  import Footer from './lib/Footer.svelte';
  import Menu from './lib/Menu.svelte';

  let active = $state(false);
</script>

<nav class={`${active ? 'active' : ''}`} id="nav">
  <Menu {active} />
  <Button bind:active />
</nav>
<Footer />

<style lang="scss">
  nav {
    background-color: #fff;
    padding: 20px;
    width: 80px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 3px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
    transition: width 0.6s linear;
    &.active {
      width: 350px;
    }
  }
</style>
