<script>
  export let name;
  export let x;
  export let y;
  export let size;

  let xpx = x+'px'
  let ypx = y+'px'

  let sizepx = size+"px";


</script>

<style>
  bubble {
    padding:  calc(var(--size)/4);
    border-radius:  var(--size);
    height: var(--size);
    width:  var(--size);
    -webkit-box-shadow: 0px 0px 40px 2px rgba(0, 0, 255,0.1);
    -moz-box-shadow: 0px 0px 40px 2px rgba(0, 0, 255, 0.1);
    box-shadow: 0px 0px 40px 2px rgba(0, 0, 255, 0.1);
    position: absolute;
    background-color: white;
    left: var(--x);
    top: var(--y);

  }
</style>

<bubble style="--x: {xpx}; --y: {ypx}; --size:{sizepx};">{name}</bubble>
