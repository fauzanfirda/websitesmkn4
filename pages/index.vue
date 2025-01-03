<template>
    <img src="../assets/home.jpg" style="width: 100%;" alt="">
    <div class="container-fluid">
    <h1 class="text-center p-5">BERITA</h1>
        <div class="row m-5 p-3">
            <div v-for="(ber, index) in berita" :key="index" class="col-3 p-3">
                <div class="card p-2" style="height:100%;">
                    <img :src="ber.foto" style="width: 100%;" alt="">
                    <h5 class="pe-2">{{ ber.judul}}</h5>
                </div>
            </div>
            <div v-for="(ber, index) in berita" :key="index" class="col-3 p-3">
                <div class="card p-2" style="height:100%;">
                    <img :src="ber.foto" style="width: 100%;" alt="">
                    <h5 class="pe-2">{{ ber.judul}}</h5>
                </div>
            </div>
            <div v-for="(ber, index) in berita" :key="index" class="col-3 p-3">
                <div class="card p-2" style="height:100%;">
                    <img :src="ber.foto" style="width: 100%;" alt="">
                    <h5 class="pe-2">{{ ber.judul}}</h5>
                </div>
            </div>
            <div v-for="(ber, index) in berita" :key="index" class="col-3 p-3">
                <div class="card p-2" style="height:100%;">
                    <img :src="ber.foto" style="width: 100%;" alt="">
                    <h5 class="pe-2">{{ ber.judul}}</h5>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
const supabase = useSupabaseClient()
const berita = ref([])

const getBerita = async () => {
  const { data, error } = await supabase
    .from('berita')
    .select('*')
  if (error) {
    console.error( error)
  } else {
    berita.value = data
  }
}

onMounted(() => {
  getBerita()
})
</script>