<template>
  <div class="container-fluid py-3 mt-5">
    <h1 class="fs-1 fw-bold font-monospace p-4 text-center mt-5">Produtos</h1>
    <div class="dropdown text-end">
      <button
        class="btn btn-primary dropdown-toggle"
        type="button"
        data-bs-toggle="dropdown"
        aria-expanded="false"
      >
        Categorias
      </button>
      <ul class="dropdown-menu">
        <li>
          <button class="dropdown-item" type="button" @click="getProducts()">
            Todas
          </button>
          <button
            class="dropdown-item"
            type="button"
            v-for="(item, index) in categories"
            :key="index"
            @click="getProductsByCategory(item)"
          >
            {{ item }}
          </button>
        </li>
      </ul>
    </div>
    <div class="row g-4">
      <div
        class="col-xl-3 col-lg-3 col-md-6 col-sm-6 col-12"
        v-for="product in products"
        :key="product.id"
      >
        <router-link :to="{ name: 'detail', params: { id: product.id } }">
          <!-- <div class="card">
            <img :src="product.image" class="card-img-top" alt="" />
            <diAddv class="card-body">
              <h5 class="card-title">{{ product.title }}</h5>
              <p class="card-text border-top border-bottom">
                <span class="fs-5">Preço: $ {{ product.price }}</span>
              </p>
            </diAddv>
          </div> -->

          <div class="card">
            <div class="card-body">
              <div class="card-img-actions">
                <img
                  :src="product.image"
                  class="card-img-top"
                  width="96"
                  height="350"
                  alt=""
                />
              </div>
            </div>

            <div class="card-body bg-light text-center">
              <div class="mb-2">
                <h6 class="font-weight-semibold mb-2">
                  <a href="#" class="text-default mb-2" data-abc="true"
                    >{{ product.title }}</a
                  >
                </h6>

                <a href="#" class="text-muted" data-abc="true">{{ product.category }}</a>
              </div>

              <h3 class="mb-0 font-weight-semibold">${{ product.price }}</h3>

              <div>
                <i class="fa fa-star star"></i>
                <i class="fa fa-star star"></i>
                <i class="fa fa-star star"></i>
                <i class="fa fa-star star"></i>
              </div>


            </div>
          </div>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "ProductList",
  data() {
    return {
      products: [],
      categories: [],
    };
  },
  mounted() {
    this.getProducts();
    this.getCategories();
  },
  methods: {
    getProducts() {
      axios.get("/products").then((response) => {
        // console.log(response);
        this.products = response.data;
      });
    },
    getCategories() {
      axios.get("/products/categories").then((response) => {
        this.categories = response.data;
      });
    },
    getProductsByCategory(name) {
      axios.get("/products/category/" + name).then((response) => {
        this.products = response.data;
      });
    },
  },
};
</script>

<style scoped>
.card {
  width: 1fr;
  height: 100%;
}

.card-img-top {
  height: 350px;
  padding: 30px;
}

.card-title {
  padding-bottom: 20px;
}

.btn {
  margin-bottom: 30px;
}

.mt-50 {
  margin-top: 50px;
}

.mb-50 {
  margin-bottom: 50px;
}

.card {
  position: relative;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-direction: column;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
  background-color: #fff;
  background-clip: border-box;
  border: 1px solid rgba(0, 0, 0, 0.125);
  border-radius: 0.1875rem;
}

.card-img-actions {
  position: relative;
}
.card-body {
  -ms-flex: 1 1 auto;
  flex: 1 1 auto;
  padding: 1.25rem;
  text-align: center;
}

.card-img {
  width: 350px;
}

.star {
  color: red;
}

.bg-cart {
  background-color: orange;
  color: #fff;
}

.bg-cart:hover {
  color: #fff;
}

.bg-buy {
  background-color: green;
  color: #fff;
  padding-right: 29px;
}
.bg-buy:hover {
  color: #fff;
}

a {
  text-decoration: none !important;
}
</style>
