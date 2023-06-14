<script>
  const pos = {
    x: 0,
    y: 0,
  }

  const mouseMoveHandler = (event) => {
    pos.x = event.x
    pos.y = event.y
  }
</script>

<div>
  <div class="playground" on:mousemove={mouseMoveHandler}>
    <h2 class="playground__pos">X: {pos.x}, Y:{pos.y}</h2>
  </div>
</div>

<style>
  .playground {
    display: flex;
    align-items: center;
    justify-content: center;
    min-width: 100%;
    min-height: 200px;
    margin-bottom: 1rem;
    border: solid 1px #000;
  }
  .playground__pos {
    font-size: 20px;
  }
</style>
