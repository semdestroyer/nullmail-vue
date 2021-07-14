<template>
  <div>
    <div class="container">
      <div class="col-md-6 mx-auto">
      <div class="card">
        <div class="card-title">Сервис временной почты NULLMAIL<i class="bi bi-watch"></i>
        </div>
        <div class="card-body">
          <i class="bi bi-envelope-open"><span class="badge rounded-pill bg-danger text-white">1</span></i>
          <timer></timer>
          <input type="text"  v-model="email" readonly>
        </div>
        <div class="card-footer">
          <button class="btn btn-primary">Получить новый Email</button>
        </div>
      </div>
      </div>
    </div>
  </div>
</template>

<script>


import Timer from "./components/Timer";
export default {
  name: 'App',
  components: {Timer},
  data(){
    return{
      email:""
    }
  },
  methods:{
    send:function()
    {

    },


  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
