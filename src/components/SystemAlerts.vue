<template>
      <div class="row system-alerts">
          <div class="col-md-12" v-for="(list,index) in listTitle" :key="list">
              <div class="card bg-dark-2">
                <div class="card-body">
                  <small>{{list}}</small> <a class="pull-right text-orange">View Details</a>
                  <div>{{ListData[index]}} </div>
                </div>
            </div>
          </div>
      </div> 

</template>

<script>
export default {
  name: 'SystemAlerts',
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
.card-body{
  padding: 10px;
}
</style>
