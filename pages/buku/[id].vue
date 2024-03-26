<template>
  <div>
    <h1>{{ buku.judul }}</h1>
    <span v-if="buku.cover"><img :src="buku.cover" :alt="buku.judul"></span>
    <span v-else><img src="https://placehold.jp/150x150.png"></span>
  </div>
</template>
    
    
    
    <script setup>
    const supabase = useSupabaseClient()
    
    const route = useRoute()
    
    const buku = ref([])
    
    const getBookById = async () => {
      const { data, error } = await supabase.from('buku').select('*, kategori(*)')
      .eq('id', route.params.id)
      if(data) buku.value = data [0]
    } 
    
    onMounted(() => {
      getBookById
    })
    </script>