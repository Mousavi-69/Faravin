<template>
<div>

  <button id="btn" @click.right.prevent="" @mousedown.right.prevent="clickdown" @mouseup.right.prevent="clickup">Hold Me 1.5 for Seconds</button>
</div>

</template>

<script>

export default {
  name: 'App',
  components: {
  },

data(){
return{
  timeId:0,
}
},
methods:{
  clickdown(){
    // console.log(event)

    this.timeId = setTimeout(function(){
     alert("1.5 ثانیه کلیک را نگه داشتید")
    },1500)
  },
  clickup(){
clearTimeout(this.timeId)
  }

}
}
</script>

<style>
  div{
    text-align: center;
  }
#btn{
  padding: 10px;
  margin-top: 200px;
  background-color: rgb(142, 135, 206);


}
</style>
