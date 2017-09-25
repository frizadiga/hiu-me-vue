<template>
<div>
  
  <!-- <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css"> -->
  
  <iframe id="content" :src="contentSRC" frameborder="0"></iframe>

  <div id="footer" class="w3-bottom w3-blue-grey">
    <input id="input-src" v-model="contentSRC" @change="changeView" class="w3-blue-grey" list="urls">
    <datalist id="urls">
      <option value="http://hiuwave.com">hiuwave</option>
      <option value="http://localhost:1700">f7-vue</option>
      <option value="https://framework7.io/kitchen-sink-material/">f7 Kitchen Sink Material</option>
    </datalist>
    <!-- <select name="" id="">
      <option value="1"></option>
      <option value="2"></option>
      <option value="3"></option>
    </select> -->
    <span id="title" class="w3-right"><b>hiuME <i class="fa fa-arrows-alt"></i></b></span>
  </div>

</div>

</html>
</template>

<script>
let content = document.getElementById('content');
let inputSRC = document.getElementById('input-src');
module.exports = {
  name:'index',
  components:{},
  data: () => ({
    contentSRC: "http://hiuwave.com"
  }),
  methods:{
    changeView: () => {
      content.src = inputSRC.value;
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
      /*z-index: 100;*/
      margin-top: 0px;
      padding: 1px 2px 1px 2px;
      /*height: 30px;*/
      /*background-color: rgb(11, 61, 73)!important;*/
      /*color: white;*/
      bottom:0;
      position: ;
    }
    #title{
      -webkit-app-region: drag;
      padding: 0px 4px 0 0  ;
    }
    #input-src{
      /*z-index: 101;*/
      -webkit-app-region: no-drag;
      height: 20px;
      width: 70%;
      border: none;
    }

</style>