<template>
  <div>
    <h2 class="text-start my-4">{{ buku.judul }}</h2>
    <div class="row">
      <div class="col-md-5">
        <span v-if="buku.cover"><img :src="buku.cover" :alt="buku.judul"></span>
      </div>
      <div class="col-md-6">
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Penulis : {{ buku.penulis }}</li>
          <li class="list-group-item">tahun_terbit : {{ buku.tahun_terbit }}</li>
          <li class="list-group-item">Penerbit: {{ buku.penerbit }}</li>
          <li class="list-group-item">rak: {{ buku.rak }}</li>
          <li class="list-group-item">{{ buku.deskripsi }}</li>
        </ul>
      </div>
    </div>
    <NuxtLink to="/buku">
      <button type="submit" class="btn btn-lg rounded-5 px5">kembali</button>
    </NuxtLink>
  </div>
</template>
    
    
    
    <script setup>
    const supabase = useSupabaseClient()
    
    const route = useRoute()
    
    const buku = ref([])
    
    const getBookById = async () => {
      const { data, error } = await supabase.from('buku').select(`*, kategori(*)`)
      .eq('id', route.params.id)
      if(data) buku.value = data [0]
    } 
    
    onMounted(() => {
      getBookById
    })
    </script>