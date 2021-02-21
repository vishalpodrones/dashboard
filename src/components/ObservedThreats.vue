<template>
<div class="row threats">
     <div class="col-md-12" v-for="(list,index) in listTitle" :key="list">
      <div class="row">
        <div class="col-md-6">
        <div>{{list}}</div>
       </div> 
       <div class="col-md-6">
          <div>{{ListData[index]}}</div>
       </div> 
       <div class="col-md-12">
         <hr/>
         </div> 
      </div> 
      </div> 
 </div> 
</template>

<script>
export default {
  name: 'ObservedThreats',
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
.threats{
   padding: 8px 8px 1px 8px;
   font-size: 12px;
}
.threats .col-md-12:first-child  .col-md-6:first-child {
  color: orangered;
}
.threats .col-md-6:nth-child(2) {
  padding: 0px;
}
.col-md-12{
      padding: 8px 8px 1px 8px;
}
.bg-dark-1{
  background-color: #0f0f0f;
}
hr {
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
    border-top: 1px solid rgb(178 178 178 / 27%);
}
.bg-dark-2{
  background-color: #181818;
}
.text-orange{
  color: #bc7548;
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
</style>
