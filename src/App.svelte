<script>

  let products = [
    {
      id: "1",
    name: "Macbook",
    description: "Laptop Macbook air",
    category: "laptops"
    },{
      id: "2",
    name: "Mouse",
    description: "mouse",
    category: "pheriperials"
    }
  ]

  let product = {
    id: "",
    name: "",
    description: "",
    category: "",
    imageURL: ""
  };

  const onSubmitHandler = e => {
    e.preventDefault();
    console.log(product);
  };
</script>

<style>

</style>

<main>

  <div class="container">
    <div class="row">
      <div class="col-md-6">
        {#each products as product}
          <li>{product.name}</li>
        {/each}
      </div>
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <form on:submit={onSubmitHandler}>

              <div class="form-group">

                <input
                  bind:value={product.name}
                  type="text"
                  placeholder="Product name"
                  id="product-name"
                  class="form-control" />

              </div>

              <div class="form-group">
                <textarea
                  bind:value={product.description}
                  id="product-description"
                  rows="3"
                  placeholder="Product description"
                  class="form-control" />
              </div>
              <div class="form-group">
                <input
                  bind:value={product.imageURL}
                  type="url"
                  id="product-image-url"
                  placeholder="https://github.com/davidnherran/sveltecrud"
                  class="form-control" />
              </div>
              <div class="form-group">
                <select
                  id="category"
                  bind:value={product.category}
                  class="form-control">
                  <option value="laptops">Laptops</option>
                  <option value="peripherials">Peripherials</option>
                  <option value="servers">Servers</option>
                </select>
              </div>
              <button class="btn btn-secondary">Save product</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>

</main>
