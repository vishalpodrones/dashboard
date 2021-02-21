<template>
  <div class="row col-md-12 mt-4">
      <div class="col-md-4">
          <i class="fa fa-bug"></i> <span>2 %</span>
          <label>Malicious Files</label>
      </div>   
      <div class="col-md-4">
          <i class="fa fa-file-archive-o"></i> <span>856</span>
          <label>Total Files Submitted</label>
      </div>   
      <div class="col-md-4">
          <i class="fa fa-file-o"></i> <span>64</span>
          <label>Total Files Bypassed</label>
      </div>   
      <div class="col-md-4">
          <i class="fa fa-search"></i> <span>63</span>
          <label>Dynamically Analysed</label>
      </div>   
      <div class="col-md-4">
          <i class="fa fa-clock-o"></i> <span class="text-success">2.3</span><small>Secs</small>
          <label>Avg Processing Time</label>
      </div>   
  </div> 
</template>

<script>
export default {
  name: 'CaptureATP',
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
span{
  font-size: 15px;
  padding: 5px;
}
label {
    font-size: 9px;
}
.col-md-4{
  padding-right: 0px;
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
