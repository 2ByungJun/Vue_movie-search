<template>
  <v-app>
    <v-container>
      <!-- 검색바 -->
      <SearchBar />
      <!-- 영화 목록 -->
      <MovieList />
    </v-container>
  </v-app>
</template>

<script>
// @ : 절대경로(Vue CLI)
// aaa
import SearchBar from '@/components/SearchBar'; 
import MovieList from '@/components/MovieList'; 
import axios from 'axios';

export default {
  components: {
    SearchBar,
    MovieList
  },
  methods: {
    
  },
  mounted(){
      console.log('mounted')
      axios.get('/api/hello').then( res => {
        console.log(res)
        console.log(res.data)
      })
    }
};
</script>
