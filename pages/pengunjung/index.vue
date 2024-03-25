<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <h2 class="text-center my-4">riwayat kunjungan</h2>
                <div class="my-3">
                    <input type="search" class="form-control from-control-lg rounded-5" placeholder="filter...">
                 </div>
                 <div class="my-3 text-muted">menampilkan 1 drat</div>
                 <table class="table table-bordered">
                    <thead>
                        <tr>
                            <td>#</td>
                            <td>NAMA</td>
                            <td>KEANGGOTAAN</td>
                            <td>KELAS</td>
                            <td>JURUSAN</td>
                            <td>TINGKAT</td>
                            <td>WAKTU</td>
                            <td>KEPERLUAN</td>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1.</td>
                            <td>Elsa Nugraha</td>
                            <td>Siswa</td>
                            <td>XI</td>
                            <td>PPLG</td>
                            <td>1</td>
                            <td>11 Maret 2024, 12.12.00</td>
                            <td>Baca Buku</td>
                        </tr>
                    </tbody>
                 </table>
            </div>
        </div>
        <NuxtLink to="/pengunjung/tambah">
            <button type="submit" class="btn btn-lg rounded-5 px-5">kembali</button>
        </NuxtLink>
    </div>
</template>

<style scoped>
.form-control{
    background-color: #DFF2F6;
}
.btn{
    background-color: #25cff4;
}
</style>