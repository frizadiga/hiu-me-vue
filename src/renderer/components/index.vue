<template>
<div>
  
  <!-- <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css"> -->
  
  <iframe id="content" src="http://localhost:1700" frameborder="0"></iframe>

  <div id="footer" class="w3-bottom w3-blue-grey">
    <h6 style="margin:0"><b>hiuME</b></h6>
  </div>

</div>

</html>
</template>

<script>
module.exports = {
  name:'index',
  components:{}
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
      -webkit-app-region: drag;
      margin-top: 0px;
      padding-left: 5px;
      padding-top: 2px;
      /*height: 30px;*/
      /*background-color: rgb(11, 61, 73)!important;*/
      /*color: white;*/
      bottom:0;
      position: fixed;
    }
</style>