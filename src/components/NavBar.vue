<template>
  <!-- <nav class="navbar navbar-expand-lg bg-light">
    <div class="container-fluid">
      <router-link class="navbar-brand fs-3" to="/">
        <img src="../assets/images/logo.svg" class="px-3" alt="" height="40" />
      </router-link>

      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item px-2 fs-5">
            <router-link to="/shop" class="nav-link" aria-current="page"
              >Produtos</router-link
            >
          </li>
          <li class="nav-item px-2 fs-5">
            <router-link to="/cart" class="nav-link" aria-current="page"
              >
              <i class="bi bi-cart"></i>
              <span class="badge text-bg-secondary">{{
                this.$store.state.cart
              }}</span></router-link
            >
          </li>
        </ul>
      </div>
    </div>
  </nav> -->

  <header
    class="main-header"
    :class="this.$route.name == 'home' ? 'transparent' : 'colored'"
  >
    <div class="header-wrapper">
      <router-link to="/" class="main-logo"
        ><img src="../assets/images/logo.svg" class="px-3" alt="" height="40"
      /></router-link>
      <nav>
        <ul class="main-menu">
          <li>
            <router-link to="/shop" class="nav-link" aria-current="page"
              >Produtos</router-link
            >
          </li>
          <li>
            <router-link to="/cart" class="nav-link" aria-current="page">
              <i class="bi bi-cart" style="font-size: 1.5em;"></i>
              <span class="badge text-bg-secondary">{{
                this.$store.state.cart
              }}</span></router-link
            >
          </li>
          <li>
            <a href="#"><span class="fa fa-search"></span></a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {};
  },
  mounted() {
    this.$store.dispatch("commitData");
  },
};
</script>

<style scoped>
.navbar-brand img {
  border-radius: 50%;
}

.nav-item {
  position: relative;
  text-decoration: none;
  color: #262626;
}

.nav-item::before {
  position: absolute;
  content: "";
  width: 100%;
  height: 3px;
  bottom: -3px;
  background-color: #262626;
  visibility: hidden;
  transform: scaleX(0);
  transition: all 0.3s ease-in-out 0s;
}

.nav-item:hover::before {
  visibility: visible;
  transform: scaleX(1);
}

.transparent {
  background: transparent;
}

.colored {
  background-color: rgba(127, 127, 127, 0.15);
  color: #000 !important
}
</style>
