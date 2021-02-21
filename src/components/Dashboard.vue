<template>
<div class="dashboard-main">
  <div class="row">
      <div class="col-md-6">
            <div class="row">
                <div class="col-md-6 pr-o">
                  <div class="card bg-dark-1">
                    <div class="card-body">
                      <div class="const-height">
                       <div class="common-card">
                       <b> CPU Utilization </b>
                        <select class="float-right">
                          <option>Day</option>
                        </select>
                       <bar-chart
                                :height="120"
                                ref="barChart"
                                :chart-data="redBarChart.chartData"
                        >
                        </bar-chart>
                      </div>

                       <h1><hr/></h1>
                       <div class="common-card">
                       <b> Sessions </b>
                        <div class="float-right">
                          213<small> / Minutes</small>
                        </div>
                        <bar-chart
                                :height="120"
                                ref="barChart"
                                :chart-data="redBarChart.chartData"
                        >
                        </bar-chart>
                       </div>
                        </div>
                    </div>
                  </div>
                </div>
                <div class="col-md-3">
                    <div class="card bg-dark-1">
                    <div class="card-body">
                        <div class="common-card">
                           <div class="const-height">
                           <b>Application Risk Level</b>
                           <bar-chart
                                    :height="120"
                                    ref="barChart"
                                    :chart-data="redBarChart.chartData"
                            >
                            </bar-chart>
                        </div>
                        </div>
                    </div>
                  </div>
                </div>
                <div class="col-md-3 pl-o pr-o">
                    <div class="card bg-dark-2">
                    <div class="card-body">
                      <div class="const-height">
                        <List v-bind:ListData="listdata3" v-bind:listSelect="listSelect3" v-bind:listcolor="listcolor3" v-bind:listpercent="listpercent3" v-bind:listTitle="listTitle3" v-bind:listcount="listcount3"></List>
                    </div>
                     </div>
                  </div>
                </div>
          </div>
    </div> 
    <div class="col-md-6">
            <div class="row">
                <div class="col-md-3 pl-o pr-o">
                    <div class="card bg-dark-2">
                      <div class="card-body">
                      <div class="const-height">
                        <List v-bind:ListData="listdata4" v-bind:listSelect="listSelect4" v-bind:listcolor="listcolor4" v-bind:listpercent="listpercent4" v-bind:listTitle="listTitle4" v-bind:listcount="listcount4"></List>
                      </div>
                       </div>
                    </div>
                </div>
                <div class="col-md-3 pl-o pr-o">
                      <div class="card bg-dark-2">
                      <div class="card-body">
                      <div class="const-height">
                         <List v-bind:ListData="listdata5" v-bind:listSelect="listSelect5" v-bind:listcolor="listcolor5" v-bind:listpercent="listpercent5" v-bind:listTitle="listTitle5" v-bind:listcount="listcount5"></List>
                         </div>
                    </div>
                   </div>
                </div>
                <div class="col-md-6">
                            <div class="card bg-dark-1">
                            <div class="card-body">
                              <div class="common-card const-height">
                              <b>System Alerts (Last 5)</b> <a class="text-orange">View All</a>
                              <select class="float-right">
                                <option>All Alerts</option>
                              </select>
                              <SystemAlerts v-bind:ListData="SysAlerts" v-bind:listTitle="SysAlerts1"></SystemAlerts>
                          </div>
                        </div>
                      </div>
                </div>
          </div>
    </div>
</div>
 <div class="row pt-3">
                <div class="col-md-v-3 col-sm-12 col-xs-12 pl-3">
                    <div class="card bg-dark-2">
                       
                      <div class="card-body">
                        <div class="const-height">
                          <List v-bind:ListData="listdata6" v-bind:listSelect="listSelect6" v-bind:listcolor="listcolor6" v-bind:listpercent="listpercent6" v-bind:listTitle="listTitle6" v-bind:listcount="listcount6"></List>
                        <hr/>
                          <List v-bind:ListData="listdata7" v-bind:listSelect="listSelect7" v-bind:listcolor="listcolor7" v-bind:listpercent="listpercent7" v-bind:listTitle="listTitle7" v-bind:listcount="listcount7"></List>
                        </div>
                         </div>
                    </div>
                </div>
                <div class="col-md-v-3 col-sm-12 col-xs-12 pr-0">
                    <div class="card bg-dark-1">
                      <div class="card-body">
                        <div class="common-card const-height">
                           <b>Insights</b>
                           <Insights v-bind:ListData="ThreatDesc" v-bind:listTitle="ThreatTitle"></Insights>
                        </div>
                      </div>
                    </div>
                </div>
                <div class="col-md-v-3 col-sm-12 col-xs-12 pl-3 pr-3">
                      <div class="card bg-dark-2">
                        <div class="card-body">
                        <div class="common-card const-height">
                           <b>Observed Threats</b>
                             <ObservedThreats v-bind:ListData="ThreatDesc" v-bind:listTitle="ThreatTitle"></ObservedThreats>
                        </div>
                        </div>
                      </div>
                </div>
                <div class="col-md-v-6 col-sm-12 col-xs-12 pl-0">
                    <div class="card bg-dark-1">
                      <div class="card-body">
                         <div class="common-card const-height">
                          <b> Capture ATP </b>
                            <select class="float-right">
                              <option>Week</option>
                            </select>
                         
                          <div class="row">
                             <CaptureATP></CaptureATP>
                          </div>
                          <div class="col-md-12">
                              <hr/>
                          </div>
                          <div class="row">
                            <div class="col-md-12">
                            <b> Verdicts (Files) </b>
                              <br/> <br/>
                           <bar-chart
                                    :height="150"
                                    ref="barChart"
                                    :chart-data="redBarChart.chartData"
                            >
                            </bar-chart>
                            </div>
                         </div>
                          </div>
                      </div>
                     
                    </div>
                </div>
                <div class="col-md-v-3  col-sm-12 col-xs-12 pl-o pr-o">
                  <div class="card bg-dark-2">
                    <div class="card-body">
                       <div class="const-height">
                          <List v-bind:ListData="listdata" v-bind:listSelect="listSelect" v-bind:listcolor="listcolor" v-bind:listpercent="listpercent" v-bind:listTitle="listTitle" v-bind:listcount="listcount"></List>
                    </div>
                     </div>
                  </div>
                </div>
                <div class="col-md-v-3 col-sm-12 col-xs-12 pl-o pr-o">
                    <div class="card bg-dark-2">
                      <div class="card-body">
                         <div class="const-height">
                         <List v-bind:ListData="listdata1"  v-bind:listSelect="listSelect1" v-bind:listcolor="listcolor1" v-bind:listpercent="listpercent1" v-bind:listTitle="listTitle1" v-bind:listcount="listcount1"></List>
                      </div>
                       </div>
                    </div>
                </div>
                <div class="col-md-v-3 col-sm-12 col-xs-12 pl-o pr-3">
                    <div class="card bg-dark-2">
                      <div class="card-body">
                         <div class="const-height">
                     <List v-bind:ListData="listdata2" v-bind:listSelect="listSelect2" v-bind:listcolor="listcolor2" v-bind:listpercent="listpercent2" v-bind:listTitle="listTitle2" v-bind:listcount="listcount2"></List>
                      </div>
                       </div>
                  </div>
             
    </div>
</div>
</div>
</template>

<script>
import List from './List.vue';
import SystemAlerts from './SystemAlerts.vue';
import ObservedThreats from './ObservedThreats.vue';
import Insights from './Insights.vue';
import CaptureATP from './CaptureATP.vue';
// import * as chartConfigs from './Charts/config';
// import LineChart from './Charts/LineChart';
import BarChart from './Charts/BarChart';
export default {
  name: 'Dashboard',
  props: {
    msg: String
  },
  components:{
    List,
    SystemAlerts,
    ObservedThreats,
    Insights,
    BarChart,
    CaptureATP
  },
  data() {
      return {
          tableData: {
            name: 'Facebook',
            visitors: '1,480',
            progress: 60,
            progressType: 'gradient-danger',
          },
          SysAlerts1: ['20:11:35 05 May 2020','18:02:47 05 May 2020','15:31:21 05 May 2020','13:16:19 05 May 2020'],
          SysAlerts: ['New Threat Found','Infrastructure Amazon CloudFront','procexp.exe has been Run in Sandbox','Configuration Audit Log Modified'],

          ThreatTitle: ['11400','7456','9830','5539','3901','5'],
          ThreatDesc: ['IPS','Botnet','GAV/AS','Sandbox','App. Risk','Vernabilities'],

          listTitle: 'Top Viruses',
          listSelect: 'By sessions',
          listcolor: '1',
          listdata: ['Torjan Horse','Power Worm','Mydoom','StormWorm','Brain'],
          listcount: ['43','41','35','34','20'],
          listpercent: ['90','75','60','55','30'],
          
          listTitle1: 'Top Instrusions',
          listSelect1: 'By sessions',
          listcolor1:  '2',
          listdata1: ['EchoReply','SSLv2.0...Hello2','OpenVPN...closure','DNSquery...com','1.0.345.6'],
          listcount1: ['9.14k','130','6','1','1'],
          listpercent1: ['90','75','60','55','30'],

          listTitle2: 'Top Botnets',
          listSelect2: 'By botnet block',
          listcolor2: '3',
          listdata2: ['98.234.167.228','192.268.2.345','75.75.812.09','1.0.345.6','87.13.187.01'],
          listcount2: ['45 GB','24 GB','21 GB','12 GB','9 GB'],
          listpercent2: ['90','75','60','55','30'],

          listTitle3: 'Top Applications',
          listSelect3: 'By sessions',
          listcolor3: '4',
          listdata3: ['General HTTPS','General DNS','General UDP','General H_S MGMT','General HTTP'],
          listcount3: ['435 k','412 k','353 k','341 k','204 k'],
          listpercent3: ['90','75','60','55','30'],

          listTitle4: 'Top Addresses',
          listSelect4: 'By sessions',
          listcolor4:  '5',
          listdata4: ['75.75.812.09','98.234.167.228','18.13.187.01','192.268.2.345','1.0.345.6'],
          listcount4: ['45 k','45 k','45 k','45 k','45 k'],
          listpercent4: ['90','75','60','55','30'],

          listTitle5: 'Top Users',
          listSelect5: 'By data received',
          listcolor5:  '6',
          listdata5: ['Admin','Admin 2','Unknown','Supervisor','Unknown1'],
          listcount5: ['45 GB','41 GB','24 GB','18 GB','5 GB'],
          listpercent5: ['90','75','60','55','30'],

          listTitle6: 'Policies  Security Rules',
          listSelect6: 'By type',
          listcolor6:  '7',
          listdata6: ['Allowed','Discarded','Dropped'],
          listcount6: ['90 %','8 %','2 %'],
          listpercent6: ['90','75','60','55','30'],
          
          listTitle7: 'NAT Rules',
          listSelect7: 'By translation',
          listcolor7:  '8',
          listdata7: ['Translation','Non-Translation'],
          listcount7: ['63 %','37 %'],
          listpercent7: ['90','75','60','55','30'],
          // bigLineChart: {
          //   allData: [
          //     [0, 20, 10, 30, 15, 40, 20, 60, 60],
          //     [0, 20, 5, 25, 10, 30, 15, 40, 40]
          //   ],
          //   activeIndex: 0,
          //   chartData: {
          //     datasets: [],
          //     labels: [],
          //   },
          //   extraOptions: chartConfigs.blueChartOptions,
          // },
          redBarChart: {
            chartData: {
              labels: ['Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
              datasets: [{
                label: 'Sales',
                data: [25, 20, 30, 22, 17, 29]
              }]
            }
          }
              
        }
    },
    methods: {
          // initBigChart(index) {
          //   let chartData = {
          //     datasets: [
          //       {
          //         label: 'Performance',
          //         data: this.bigLineChart.allData[index]
          //       }
          //     ],
          //     labels: ['May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
          //   };
          //   this.bigLineChart.chartData = chartData;
          //   this.bigLineChart.activeIndex = index;
          // }
        }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@media (min-width: 768px){
  .col-md-v-3 {
      flex: 0 0 12.5%;
      max-width: 12.5%;
      position: relative;
      width: 100%;
      padding-right: 7.5px;
      padding-left: 7.5px;
  }
  .col-md-v-6 {
      flex: 0 0 25%;
      max-width: 25%;
      position: relative;
      width: 100%;
      padding-right: 15px;
      padding-left: 7.5px;
  }
}
hr {
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
    border-top: 1px solid rgb(178 178 178 / 27%);
}
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
.const-height{
    width: 100%;
    float: left;
    height: 320px;
}
select {
    background: no-repeat;
    color: #fff;
    padding-right: 10px;
    border: 0;
    border-bottom: 1px solid;
}
.progress,.progress-bar {
    height: 8px!important;
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
.text-orange{
  color: #bc7548;
}
.card-body{
  padding: 1rem;
}
.common-card b{
   font-size: 10px;
}
.system-alerts{
  
}
</style>
