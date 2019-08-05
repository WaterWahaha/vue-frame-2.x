<template>
  <div class="index">
    <h1>{{ msg }}</h1>
    <h1>{{ time }}</h1>
  </div>
</template>

<script>
  import {get} from "../utils/request.js"
export default {
  name: 'index',
  data () {
    return {
      msg: 'A Public VUE Frame',
      time:'2019-8-5 10:30:00'
    }
  },
  mounted(){
    //更新时间
    this.get(host.url+'/newtime').then((res)=>{
      console.log(res)
    })
  },
  methods:{
    get,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
</style>
