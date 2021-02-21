<template>
<div class="col-md-12">
      <div class="row mt-4">
        <div class="col-md-3">
         <img src="../assets/insight1.png" alt="insight1">
       </div> 
       <div class="col-md-9">
         <div class="text-red">2</div>
          <div>Infected Hosts</div>
       </div> 
       <div class="col-md-12">
         <hr/>
         </div> 
      </div> 
       <div class="row">
        <div class="col-md-3">
         <img src="../assets/insight2.png" alt="insight1">
       </div> 
       <div class="col-md-9">
         <div class="text-red">43</div>
          <div>Critical Alerts</div>
       </div> 
       <div class="col-md-12">
         <hr/>
         </div> 
      </div> 
       <div class="row">
        <div class="col-md-3">
         <img src="../assets/insight3.png" alt="insight1">
       </div> 
       <div class="col-md-9">
         <div class="text-red">22</div>
          <div>Encrypted Traffic</div>
       </div> 
      </div>   
      </div> 
</template>

<script>
export default {
  name: 'Insights',
  props: ['listTitle','ListData'],
  data() {
      return {
        // listd: ['314k']
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.col-md-12{
      padding: 8px 8px 1px 8px;
}
.bg-dark-1{
  background-color: #0f0f0f;
}
.bg-dark-2{
  background-color: #181818;
}
.text-orange{
  color: #bc7548;
}
hr {
    border-top: 1px solid rgb(255 255 255 / 18%);
}
.card-body{
    padding: 0.5rem !important;
}
td {
    color: #fff;
}
.table {
    margin-top: 15px;
    color: #212529;
}
.text-red{
    color: orangered;
    font-size: 15px;
}
.col-md-9{
  padding: 5px;
}
</style>
