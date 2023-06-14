<script>
  let catSrc =
    'https://i.natgeofe.com/n/548467d8-c5f1-4551-9f58-6817a8d2c45e/NationalGeographic_2572187_square.jpg'
  let altText = 'Cat'
</script>

<div class="cat-pic">
  <img src={catSrc} alt={altText} class="cat-pic__img" />
</div>

<style>
  .cat-pic {
    border: solid 1px blue;
  }
  .cat-pic__img {
    max-width: 200px;
  }
</style>
