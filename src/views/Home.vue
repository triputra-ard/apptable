<template>
  <section class="container p-1 mb-20">
    <!-- matches -->
    <div class="first-box cream col-xl-12 mb-1 ">
      <div class="col-xl-3 box black">
        
      </div>
      <div class="col-xl-3 box blue">
        
      </div>
    </div>
    
    <!-- matches -->
    <div class="second-box col-xl-12 mb-1 pr-none pl-none">
      <div class="col-xl-3 box stretch blue border-2"></div>
      <div class="col-xl-6 box stretch column">
        <div class="box small-stretch orange border-2 mb-1"></div>
        <div class="box h-auto blue border-2 p-1 flex in-center mb-1">
          <div class="box small mr-1 ml-1 orange"></div>
          <div class="box small mr-1 ml-1 black"></div>
          <div class="box small mr-1 ml-1 yellow"></div>
          <div class="box small mr-1 ml-1 green"></div>
        </div>
      </div>
      <div class="col-xl-3 box stretch blue border-2 p-0">
        <div class="box red float-top"></div>
      </div>
    </div>
    
    <!-- matches -->
    <div class="col-xl-12 third-box border-2 mb-1 p-none">
      <div class="col-xl-3 box h-auto red pr-none">
        
      </div>
      <div class="col-xl-9 box h-auto cream pl-none flex in-center p-2">
        <div class="col-xl-2 box small red mr-1 ml-1"></div>
        <div class="col-xl-2 box small red mr-1 ml-1"></div>
        <div class="col-xl-2 box small red mr-1 ml-1"></div>
        <div class="col-xl-2 box small red mr-1 ml-1"></div>
        <div class="col-xl-2 box small red mr-1 ml-1"></div>
      </div>
    </div>
    
    <div class="col-xl-12 fourth-box p-none">
      <div class="col-xl-4 box small-stretch orange border-2 p-none">
        <div class="box red float-left-top"></div>
        <div class="box red float-right-top">
          <div class="box black float-right-center-top"></div>
        </div>
        <div class="box red float-bottom-right"></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Home'
}
</script>
<style scoped="">
  .cream{
    background: #ffe191;
  }
  .blue{
    background: #2b77bf;
  }
  .black{
    background: #454054;
  }
  .yellow{
    background: #fcf62b;
  }
  .red{
    background:#ff0059;
  }
  .green{
    background: #2bb800;
  }
  .orange{
    background: #ffcc42;
  }
  .box{
    height: 50px
  }
  .box.h-auto{
    height: auto!important;
  }
  .box.small{
    width: 50px;
  }
  .box.stretch{
    height: 48vh!important;
  }
  .box.float-top{
    position: relative;
    top: 0;
    width: 100%;
  }
  .box.small-stretch{
    height: 40vh!important;
  }
  .box.float-left-top{
    position: relative;
    top: 0;
    left: 0;
    width: 50%;
  }
  .box.float-right-top{
    position: relative;
    top: -50px;
    right: -230px;
    width: 50%; 
  }
  .box.float-bottom-right{
    width: 50%;
    position: relative;
    right: -230px;
    bottom: -213px;
  }
  .box.float-right-center-top{
    height: 20px!important;
    position: relative;
    top: 17px;
    right: -130px;
  }
  .border-2{
    border: 2px solid #22282e;
  }
  .p-none{
    padding: 0!important 
  }
  .pr-none{
    padding-right: 0!important;
  }
  .pl-none{
    padding-left: 0!important;
  }
  .flex{
    display: flex;
    flex-wrap: wrap;
  }
  .in-center{
    justify-content: center;
  }
  .first-box{
    height: auto;
    padding: 10px 25px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    flex-direction: row;
    border:2px solid #464345;
  }
  .second-box{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
  .third-box{
    height: auto;
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
  }
</style>