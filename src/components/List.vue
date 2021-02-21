<template>
     <div class="common-card">
          <b>{{listTitle}}</b><br/>
          <select >
            <option>{{listSelect}}</option>
          </select>
            <div class="prog-main" v-for="(list,$index) in ListData" :key="list">
              <div class="prog-section">
                <label class="custom-label">{{list}}</label>
                <div class="progress">
                  <div class="progress-bar" :class="getBgColor(listcolor)" :style="getWidth(listpercent[$index])"></div>
                </div>
              </div>
              <div class="prog-label">
                  {{listcount[$index]}}
              </div>
            </div>
          </div>

</template>

<script>
export default {
  name: 'List',
  props: ['ListData','listTitle','listcount','listpercent','listcolor','listSelect'],
  data() {
      return {
        listd: ['314k'],
        lwidth: '70%',
        classes: ['bg-blue', 'bg-indigo', 'bg-purple', 'bg-pink', 'bg-red', 'bg-orange', 'bg-yellow', 'bg-green', 'bg-cyan']
      }
    },
     computed: {
      // style () {
      //   return 'width: ' + this.lwidth ;
      // }
    },
     methods: {
      getBgColor: function(index) {
        // Get length of  classes array
        let length = this.classes.length;

        // Get the current turn (how many times the classes have been used from start to finish)
        let turn = Math.floor(index / length);

        // Multiply turn by the length then subtract result from current index
        let colorIndex = index - (turn * length);

        return this.classes[colorIndex];
      },
      getWidth: function(index1) {
       return 'width: ' + index1+'%';
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.dashboard-main{
  padding: 10px;
  background-color: #262626;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.pr-o{
  padding-right: 0;
}
.pl-o{
  padding-left: 0;
}
.card{
  border-radius: 0rem !important;
}
.bg-dark-1{
  background-color: #0f0f0f;
}
.bg-dark-2{
  background-color: #181818;
}
.common-card{
  color: #ffffff;
  text-align: left;
}
select {
    background: no-repeat;
    color: #fff;
    padding-right: 10px;
    border: 0;
    border-bottom: 1px solid;
}
.progress,.progress-bar {
    height: 1px!important;
}
.prog-section{
    width: 65%;
    display: inline-block;
    float: left;
}
.prog-label{
    width: 35%;
    display: inline-block;
    float: left;
    padding: 20px 0px 0px 10px;
}
.custom-label{
    margin-bottom: 0;
    font-size: 9px;
    margin-top: 10px;
    color: #b4b4b4;
}
.prog-main {
    margin-top: 12px;
    color: #d5d5d5;
    width: 100%;
    float: left;
}
.common-card b{
   font-size: 10px;
}
.bg-blue {
  background-color: blue;
}

.bg-indigo {
  background-color: indigo;
}

.bg-purple {
  background-color: purple;
}

.bg-pink {
  background-color: pink;
}

.bg-red {
  background-color: red;
}

.bg-orange {
  background-color: orange;
}

.bg-yellow {
  background-color: yellow;
}

.bg-green {
  background-color: green;
}

.bg-cyan {
  background-color: cyan;
}
</style>
