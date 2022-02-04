<script>
  export let name = "home";
  export let size = 28;
  let style = `font-size: ${size}px;`;
</script>

<svg class="icon icon-{name}" style={style}>
  <use xlink:href="#icon-{name}" />
</svg>

<style global>
  .icon {
    display: inline-block;
    width: 1em;
    height: 1em;
    stroke-width: 0;
    stroke: currentColor;
    fill: currentColor;
  }
</style>
