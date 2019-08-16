<template>
  <div class="home">
    {{ datas }}
  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios';
export default {
  name: 'home',
  data(){
    return {
       datas:[]
    }
  },
  mounted(){
    axios.get('http://localhost:3000/api/user').then((response)=>{
      this.datas = response.data
    })
  }
}
</script>
