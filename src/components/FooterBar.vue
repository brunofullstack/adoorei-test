<template>
  <footer class="customnav-color bg-ligth graycolor">
    <div class="container py-5">
      <div class="row gy-5">
        <div class="col-xl-8 col-lg-8 col-md-12 col-sm-12 col-12">
          <img src="../assets/images/logo.svg" alt="" class="img-fluid logo" />
          <div class="my-3">
            <span class="h4 text-white"> Bruno Carvalho Teixeira </span>
          </div>

          <p>Teste prático para vaga de desenvolvedor Frontend na Adoorei.</p>
        </div>
        <div class="col-xl-4 col-lg-4 col-md-4 col-sm-12 col-12">
          <p class="text-uppercase h5 text-white mb-4">Candidato</p>
          <p class="mb-0">Nome: Bruno Carvalho Teixeira.</p>
          <p class="mb-0">Fone: +55 48 998410425</p>
          <p class="mb-0">Email: brunofullstack@gmail.com</p>
        </div>
      </div>
    </div>
    <hr class="bg-light col-12" />
    <div class="container py-3">
      <div class="row">
        <div class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-12">
          <p class="graycolor">Copyleft © 2023.</p>
        </div>
        <div class="col-xl-6 col-lg-6 col-md-6 col-sm-12 col-12 text-end">
          <img src="../assets/images/visa.png" alt="" class="img-fluid" />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterBar",
};
</script>

<style scoped>
.graycolor {
  color: #999;
}

.mainColor {
  color: #eb3e32;
}

.logo {
  border-radius: 50%;
  width: 150px;
}
</style>
