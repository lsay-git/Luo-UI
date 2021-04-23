<template>
  <div class="about">
    <h1>{{this.msg}}</h1>
  </div>
</template>
<script>
export default {
  data(){
    return{
      msg:''
    }
  },
  created(){
    this.getTest();
  },
  methods:{
    getTest(){
      this.api({
        url: "/simple",
        method: "get"
      }).then(data =>{
        this.msg = data;
      })
    }
  }
}
</script>>
