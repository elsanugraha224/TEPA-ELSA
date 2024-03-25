<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <h2 class="text-center my-4">isi buku kunjungan</h2>
                <form>
                    <div class="mb-3">
                        <input type="text" class="form-control form-control-lg rounded-5" placeholder="nama...">
                    </div>
                    <div class="mb-3">
                        <select class="form-control form-control-lg form-select rounded-5">
                            <option value="">keanggotaan</option>
                            <option value="Siswa">Siswa</option>
                            <option value="Guru">Guru</option>
                            <option value="Staf">Staf</option>
                            <option value="Umum">Umum</option>
                        </select>
                    </div>
                    <div class="mb-3">
                        <div class="row">
                            <div class="col-md-4">
                                <select class="form-control form-control-lg form-select rounded-5 mb-2">
                                    <option value="">Tingkat</option>
                                    <option value="X">X</option>
                                    <option value="XI">XI</option>
                                    <option value="XII">XII</option>
                                </select>
                            </div>
                            <div class="col-md-4">
                                <select class="form-control form-control-lg form-select rounded-5 mb-2">
                                    <option value="">Jurusan</option>
                                    <option value="PPLG">PPLG</option>
                                    <option value="TJKT">TJKT</option>
                                    <option value="TSM">TSM</option>
                                    <option value="DKV">DKV</option>
                                    <option value="TOI">TOI</option>
                                </select>
                            </div>
                            <div class="col-md-4">
                                <select class="form-control form-control-lg form-select rounded-5 mb-2">
                                    <option value="">kelas</option>
                                    <option value="1">1</option>
                                    <option value="2">2</option>
                                    <option value="3">3</option>
                                    <option value="4">4</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    <div class="mb-3">
                        <select class="form-control form-control-lg form-select rounded-5">
                            <option value="">Keperluan</option>
                            <option value="baca">baca buku</option>
                            <option value="pinjam">pinjam buku</option>
                            <option value="kembalikan">Kembalikan buku</option>
                        </select>
                    </div>
                    <NuxtLink to="/pengunjung">
                        <button type="submit" class="btn btn-lg rounded-5 px-5">kirim</button>
                    </NuxtLink>
                    <from @sumbit.prevent="kirimData">
                    <input v-model="from.nama" type="text" placeholder="NAMA...">
                    <select v-model="from.tingkat"></select>
                    </from>
                </form>
            </div>
        </div>
    </div>
</template>
<script setup>
const supabase = useSupabaseClient()

const members = ref([])
const objectives = ref([])

const form = ref({
    nama: "",
    keanggotaan: "",
    tingkat: "",
    jurusan: "",
    kelas: "",
    keperluan: "",
});

const kirimData = async () => {
    const { error } = await supabase.from('pengunjung').insert([from.value])
    if(!error) navigateTO('/pengunjung')
};

const getKeanggotaan = async () => {
    const{data,error}=await supabase.from('keanggotaan').select('*')
    if(data) members.value=data
}

const getKeperluan = async () => {
    const{data,error}=await supabase.from('keperluan').select('*')
    if(data) members.value=data
}

onMounted(() =>{
    getKeanggotaan
    getKeperluan
})
</script>

<style scoped>
.form-control{
    background-color: #DFF2F6;
}
.btn{
    background-color: #25cff4;
}
</style>