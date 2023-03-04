<template>
    <div class="container">
      <div class="row">
        <div class="col-md-3" v-for="product in products" :key="product.id">
          <div class="card">
            <img width="200" height="200" :src="product.image" class="card-img-top" alt="Product Image">
            <div class="card-body">
              <h5 class="card-title">{{ product.name }}</h5>
              <p class="card-text">{{ product.price }} € 
                <a href="#">Voir</a>
            </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
  <div class="row justify-content-center">
    <div class="col-md-6">
      <div class="card">
        <div class="card-header">
          <h3 class="text-center">Add a Product</h3>
        </div>
        <div class="card-body">
          <form v-on:submit.prevent="addProduct(newProduct)">
            <div class="form-group">
              <label for="productname">Product Name</label>
              <input v-model="newProduct.name" type="text" class="form-control" id="productname">
            </div>
            <div class="form-group">
              <label for="productprice">Product Price</label>
              <input v-model="newProduct.price" type="number" class="form-control" id="productprice">
            </div>
            <div class="form-group">
              <label for="productimage">Product Image URL</label>
              <input v-model="newProduct.image" type="text" class="form-control" id="productimage">
            </div>
            <button type="submit" class="btn btn-primary">Submit</button>
          </form>
        </div>
      </div>
    </div>
  </div>
</div>


  </template>

<script>
export default {
  name: 'ProductsList',
  data() {
    const imgPath = '../assets/images/';
    return {
      products: [
        {
          id: 1,
          name: 'Product 1',
          price: 10,
          image: 'https://cdn.monoprix.fr/cdn-cgi/image/width=600,quality=80,format=auto,metadata=none/assets/images/fashion/3612305316914/1/1900x1900.jpg',
        },
        {
          id: 2,
          name: 'Product 2',
          price: 15,
          image: 'https://media.i-run.fr/2022/Marques/Nike/Trail/2022-11-01/Nike-Zegama.png',
        },
        {
          id: 3,
          name: 'Product 3',
          price: 20,
          image: 'https://images.radio-canada.ca/q_auto,w_844/v1/alimentation/ingredient/16x9/mangue-ingredients-mordu.jpg',
        },
        {
          id: 5,
          name: 'Product 1',
          price: 10,
          image: 'https://cdn.monoprix.fr/cdn-cgi/image/width=600,quality=80,format=auto,metadata=none/assets/images/fashion/3612305316914/1/1900x1900.jpg',
        },
        {
          id: 4,
          name: 'Product 3',
          price: 20,
          image: 'https://images.radio-canada.ca/q_auto,w_844/v1/alimentation/ingredient/16x9/mangue-ingredients-mordu.jpg',
        },
        {
          id: 6,
          name: 'Product 4',
          price: 30,
          image: 'https://images-na.ssl-images-amazon.com/images/I/71sgF5NwG6S._AC_SX679_.jpg',
        },
      ],
      newProduct: {
        name: '',
        price: '',
        image: '',
      },
    };
  },
  methods: {
    addProduct(product) {
      if (product.name && product.price && product.image) {
        product.id = this.products.length + 1;
        this.products.push(product);
        this.newProduct = {
          name: '',
          price: '',
          image: '',
        };
        alert('Product added successfully');
      } else {
        alert('Please fill all fields');
      }
    },
  },
};
</script>


<style>

</style>