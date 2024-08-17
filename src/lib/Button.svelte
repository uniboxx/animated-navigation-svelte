<script>
  let { active = $bindable() } = $props();
</script>

<button
  class={`icon ${active ? 'active' : ''}`}
  id="toggle"
  onclick={() => (active = !active)}>
  <div class="line line1"></div>
  <div class="line line2"></div>
</button>

<style lang="scss">
  .icon {
    background-color: #fff;
    border: 0;
    cursor: pointer;
    padding: 0;
    position: relative;
    height: 30px;
    width: 30px;
    &:focus {
      outline: 0;
    }
    .line {
      background-color: #5290f9;
      height: 2px;
      width: 20px;
      position: absolute;
      top: 10px;
      left: 5px;
      transition: transform 0.6s linear;
    }
    .line2 {
      top: auto;
      bottom: 10px;
    }
    &.active {
      .line1 {
        transform: rotate(-765deg) translateY(5.5px);
      }
      .line2 {
        transform: rotate(765deg) translateY(-5.5px);
      }
    }
  }
</style>
