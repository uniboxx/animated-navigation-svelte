<script>
  let { item, active } = $props();
</script>

<li class={`${active ? 'active' : ''}`}>
  <a href="#">{item}</a>
</li>

<style lang="scss">
  li {
    transform: rotateY(0deg);
    opacity: 0;
    transition:
      tranform 0.6s linear,
      opacity 0.6s linear;

    a {
      position: relative;
      color: #000;
      text-decoration: none;
      margin: 0 10px;
    }
    &.active {
      opacity: 1;
      transform: rotateY(360deg);
    }
  }
</style>
