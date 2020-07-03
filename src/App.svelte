<script>
  let product = { 
	  id: "", 
	  name: "", 
	  description: "", 
	  category: "", 
	  imageURL: "" };
</script>

<style>

</style>

<main>

  <form action="">
    <input bind:value={product.name} type="text" placeholder="Product name" id="product-name" />
    <textarea
      bind:value={product.description}
      id="product-description"
      rows="3"
      placeholder="Product description" />
    <input
      bind:value={product.imageURL}
      type="url"
      id="product-image-url"
      placeholder="https://github.com/davidnherran/sveltecrud" />
    <select id="category" bind:value={product.category}>
      <option value="laptops">Laptops</option>
      <option value="peripherials">Peripherials</option>
      <option value="servers">Servers</option>
    </select>
    <button>Save product</button>
  </form>

</main>
