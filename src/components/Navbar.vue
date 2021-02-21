<template>
<nav class="navbar navbar-custom navbar-expand-sm bg-dark navbar-dark">
  <!-- Brand/logo -->
  <a class="navbar-brand" href="#">
    <i class="fa fa-tachometer" aria-hidden="true"></i> DASHBOARD
  </a>
  <!-- Toggler/collapsibe Button -->
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#collapsibleNavbar1">
    <span class="navbar-toggler-icon"></span>
  </button>
  <!-- Links -->
    <div class="collapse navbar-collapse" id="collapsibleNavbar1">
      <ul class="navbar-nav ml-auto">
        <li class="nav-item">
          <a class="nav-link" href="#"><i class="fa fa-magic" aria-hidden="true"></i></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#"><i class="fa fa-clock-o" aria-hidden="true"></i><sup><span class="badge badge-danger">6</span></sup></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#"><i class="fa fa-lightbulb-o" aria-hidden="true"></i></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#"><span class="badge badge-secondary">AD</span></a>
        </li>
      </ul>
    </div>
</nav>
</template>

<script>
export default {
  name: 'Navbar',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
.fa{
   color: #ffffff;
     font-size: 15px;
}
.fa-clock-o {
    color: #e77e3a;
}
i.fa.fa-tachometer {
    color: #e77e3a;
       font-size: 15px;
       padding: 8px;
}
a.navbar-brand, .navbar-dark {
    font-size: 13px;
    padding: 3px 14px;
    background-color: #000000 !important;
}
.fa-magic{
  -webkit-transform: scaleX(-1);
  transform: scaleX(-1);
}
.navbar-nav li {
    display: inline-block;
    margin: 0;
}
.badge-secondary {
    color: #fff;
    background-color: #6c757d;
    border-radius: 50%;
    line-height: 1.7;
}
</style>
