<template>
<div>
  
  <!-- <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css"> -->
  
  <iframe id="content" :src="contentSRC" frameborder="0"></iframe>

  <div id="footer" class="w3-bottom w3-blue-grey">
    <i class="fa fa-bars"></i> 
    <input type="text" id="input-src" v-model.lazy="contentSRC" :value="contentSRC" class="w3-blue-grey" list="urls" placeholder=" Target URL here...">
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
const content = document.getElementById('content');
const inputSRC = document.getElementById('input-src');
module.exports = {
  name:'index',
  components:{},
  data: () => ({
    contentSRC: "http://hiuwave.com/parallax"
  }),
  methods:{
    changeView: () => {
      // alert('changeView');
      return this.contentSRC = document.getElementById('input-src').value;
    }
  }
}
</script>

<style>
.content::-webkit-scrollbar {
    width: 5px!important;
}
 
iframe body::-webkit-scrollbar-track {
    -webkit-box-shadow: inset 0 0 5px rgba(0,0,0,0.3);
}
 
iframe body::-webkit-scrollbar-thumb {
  background-color: darkgrey;
  outline: 1px solid slategrey;
}

 iframe::-webkit-scrollbar {  
    display: none;
  }  
    /*body{
      height: 100%;
      width: 100%;
      background-color: white;
    }*/
    #content{
      z-index: -1;
      width: 100%;
      height: 693.019px;
      /*height: 100vh;*/
    }
    #footer{
      z-index: 100;
      margin-top: 0px;
      padding: 1px 2px 1px 6px;
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
      z-index: 101;
      -webkit-app-region: no-drag;
      height: 20px;
      width: 70%;
      border: none;
    }

</style>