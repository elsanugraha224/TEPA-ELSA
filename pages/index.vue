<template>
    <div class="container-fluid">
        <div class="row my-5">
            <div class="col-lg-6 box">
                <nuxt-link to="../pengunjung/tambah">
                    <div class="card bg-pengunjung rounded-5">
                        <div class="card-body">
                            <h2>Pengunjung</h2>
                        </div>
                    </div>
                </nuxt-link>
            </div>
            <div class="col-lg-6 box">
                <nuxt-link to="../buku">
                    <div class="card bg-buku rounded-5">
                        <div class="card-body">
                            <h2>Cari Buku</h2>
                        </div>
                    </div>
                </nuxt-link>
            </div>
        </div>
    </div>
    <h2 style="margin: 30px"><strong>STATISTIK</strong></h2>
  <div class="Container-fluid">
    <div class="row justify-content-evenly rounded-3">
      <div class="col-5">
        <div class="card1">
          <div class="raccing">
            <h1>3</h1>
            <h5>Pengunjung</h5>
          </div>
        </div>
      </div>
      <div class="col-5">
        <div class="raccing1">
          <h1>180</h1>
          <h5>Buku</h5>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
    height: 250px;
    box-shadow: 1px 1px 10px #424242;
}
.card.bg-pengunjung {
    background-image: url('../assets/img/bg-home-kunjungan (1) (1).jpeg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
}
.card.bg-buku {
    background: url('../assets/img/bg-home-cari-buku (3).jpg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
}
.raccing {
  height: 200px;
  box-shadow: 1px 1px 10px;
  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color:#F5C9E4;
}
.raccing1 {
  height: 200px;
  box-shadow: 1px 1px 10px;
  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #C0F2EC;
}
.card-body h2{
    color: black;
}
.box {
  width: 50%;
}
.box a{
  text-decoration: none;
}
h5{
  padding-top: 10px;
}
</style>