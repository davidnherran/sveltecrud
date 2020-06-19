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
    <input type="text" placeholder="Product name" id="product-name" />
    <textarea
      id="product-description"
      rows="3"
      placeholder="Product description" />
    <input
      type="url"
      id="product-image-url"
      placeholder="https://github.com/davidnherran/sveltecrud" />
    <button>Save product</button>
  </form>

</main>
