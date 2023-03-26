<template>
  <div class="container my-4">
    <div class="row g-5">
      <div
        class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-12 position-relative"
      >
        <img
          src="../assets/images/men-category.jpg"
          alt=""
          class="img-fluid category-img"
        />
        <div class="position-absolute top-50 start-50 category">
          <h3>Roupas masculinas</h3>
          <router-link
            :to="{ name: 'category', params: { name: 'men\'s clothing' } }"
            class="btn text-decoration-none text-light text-uppercase"
            aria-current="page"
            role="button"
            >Compre agora</router-link
          >
        </div>
      </div>
      <div
        class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-12 position-relative"
      >
        <img
          src="../assets/images/women-category.jpg"
          alt=""
          class="img-fluid category-img"
        />
        <div class="position-absolute top-50 start-50 category">
          <h3>Roupas femininas</h3>
          <router-link
            :to="{ name: 'category', params: { name: 'women\'s clothing' } }"
            class="btn text-decoration-none text-light text-uppercase"
            aria-current="page"
            role="button"
            >Compre agora</router-link
          >
        </div>
      </div>
      <div
        class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-12 position-relative"
      >
        <img
          src="../assets/images/jewel-category.jpg"
          alt=""
          class="img-fluid category-img"
        />
        <div class="position-absolute top-50 start-50 category">
          <h3>Jóias</h3>
          <router-link
            :to="{ name: 'category', params: { name: 'jewelery' } }"
            class="btn text-decoration-none text-light text-uppercase"
            aria-current="page"
            role="button"
            >Compre agora</router-link
          >
        </div>
      </div>
      <div
        class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-12 position-relative"
      >
        <img
          src="../assets/images/electronic-category.jpg"
          alt=""
          class="img-fluid category-img"
        />
        <div class="position-absolute top-50 start-50 category">
          <h3>Produtos eletrônicos</h3>
          <router-link
            :to="{ name: 'category', params: { name: 'electronics' } }"
            class="btn text-decoration-none text-light text-uppercase"
            aria-current="page"
            role="button"
            >Compre agora</router-link
          >
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ProductCategory",
};
</script>
<style scoped>
.container {
  color: white;
}

.category {
  backdrop-filter: blur(1px);
  padding: 10px;
  border-radius: 15px;
}

.category-img {
  width: 100vw;
  height: 400px;
  object-fit: cover;
  border-radius: 10px;
}
</style>
