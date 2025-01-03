<template>
    <div class="container-fluid">
    <h1 class="mt-5 text-center">galeri</h1>
    <div class="row p-5 m-5">
    <div v-for="(foto, index) in galeri" :key="index" class="col-3 p-5">
    <img :src="foto.foto" style="width: 100%; height:200px;" alt="">
    </div>
    </div>
    </div>
</template>
<script setup>
const supabase = useSupabaseClient()
const galeri = ref([])

const getGaleri = async () => {
  const { data, error } = await supabase
    .from('galeri')
    .select('*')
  if (error) {
    console.error( error)
  } else {
    galeri.value = data
  }
}

onMounted(() => {
  getGaleri()
})
</script>