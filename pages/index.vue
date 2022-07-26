<template>
  <div>
    <div class="container px-4 py-5" id="featured-3">
      <Judul> Ini Judul Satu </Judul>
      <Judul> {{ search }} </Judul>

      <div>
        <input type="text" v-model="search" />
      </div>

      <div v-if="isLoading">Lagi loading....</div>
      <div class="row g-4 py-5 row-cols-1 row-cols-lg-3" v-if="!isLoading">
        <BlogItem v-for="item in filteredList" :key="item.id">
          {{ item.title }}
        </BlogItem>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      isLoading: true,
      blogItems: [],
      search: '',
    }
  },
  computed: {
    filteredList() {
      return this.blogItems.filter((post) => {
        return post.title.toLowerCase().includes(this.search.toLowerCase())
      })
    },
  },
  mounted() {
    this.getBlogItem()
  },

  methods: {
    async getBlogItem() {
      this.isLoading = true
      const response = await this.$axios.get(
        'https://jsonplaceholder.typicode.com/posts'
      )

      console.log('getBlogItem', response)

      this.blogItems = response.data

      this.isLoading = false
    },
  },
}
</script>
