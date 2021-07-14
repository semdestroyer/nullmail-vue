<template>
<h6>{{minutes + ":" + seconds}}</h6>
</template>

<script>
export default {
  name: "Timer",
  data()
  {
    return{
      minutes:10,
      seconds:0,
      allseconds:0,
    }
  },
  methods:{
    showTime:function() {
      setInterval(()=>{
        this.allseconds -= 1;
        this.minutes = Math.floor(this.allseconds/60);
        this.seconds = this.allseconds % 60;
      },1000);
    }
  },
  mounted() {
    this.allseconds = this.minutes * 60;
    this.showTime();
  }
}
</script>

<style scoped>

</style>