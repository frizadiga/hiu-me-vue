<template>
<div>
  
  <!-- <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css"> -->
  
  <iframe id="content" :src="contentSRC" frameborder="0"></iframe>

  <div id="footer" class="w3-bottom w3-blue-grey">
    <input type="text" id="input-src" v-model="contentSRC" class="w3-blue-grey">
    <span id="title" class="w3-right"><b>hiuME <i class="fa fa-arrows-alt"></i></b></span>
  </div>

</div>

</html>
</template>

<script>

module.exports = {
  name:'index',
  components:{},
  data: () => ({
    contentSRC: "http://hiuwave.com"
  }),
  methods:{
    changeView: () => {
      content.src = input.value;
    }
  }
}
</script>

<style scoped>
    
    body{
      height: 100%;
      width: 100%;
      background-color: white;
    }
    #content{
      width: 100%;
      height: 693.019px;
      /*height: 100vh;*/
    }
    #footer{
      margin-top: 0px;
      padding: 1px 2px 1px 2px;
      /*height: 30px;*/
      /*background-color: rgb(11, 61, 73)!important;*/
      /*color: white;*/
      bottom:0;
      position: fixed;
    }
    #title{
      -webkit-app-region: drag;
      padding: 0px 4px 0 0  ;
    }
    #input-src{
      -webkit-app-region: no-drag;
      height: 20px;
      width: 70%;
      border: none;
    }

</style>