<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <h2 class="text-center my-4">CARI BUKU</h2>
        <div class="my-3">
          <input type="search" class="form-control rounded-5" placeholder="Mau baca apa hari ini?">
        </div>
        <div class="my-3 text-muted">menampilkan 3 dari 3</div>
        <div class="row justify-content-evenly">
          <div class="col-lg-2">  
            <div class="card mb-3">
              <div class="card-body">
                <img src="~/assets/img/cover.jpg" class="cover" alt="cover">
              </div>
            </div>
          </div>
          <div class="col-lg-2">
            <div class="card mb-3">
              <div class="card-body">
                <img src="~/assets/img/cover2.jpg" class="cover" alt="cover2">
              </div>
            </div>
          </div>
          <div class="col-lg-2">
            <div class="card mb-3">
              <div class="card-body">
                <img src="~/assets/img/cover3.jpg" class="cover" alt="cover3">
              </div>
            </div>
          </div>
            </div>
          </div>
        </div>
      </div>
    <nuxt-link to="/">
    <button type="button" class="from-kembali btn btn-secondary btn-lg rounded-5px-5">KEMBALI</button></nuxt-link>
</template>


<style scoped>
.card-body {
  width: 100%;
  height: 30em;
  padding: 0;
}
.cover {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: 0 30;
}
.form-control{
  background-color: rgb(172, 169, 175);
}
.form-kembali{
  background-color: rgb(172, 169, 175);
}
</style>