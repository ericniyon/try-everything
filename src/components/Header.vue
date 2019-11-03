<template>
 <header>
     <h1 v-on:click='ChangeTitle'>  {{ title }}</h1>
 </header>
</template>

<script>

export default {
  props:{
    title:{
      type:String
    }
  },
  data () {
    return {
     her: ' My '
    }
  },
  methods:{
    ChangeTitle:function(){
      this.$emit('ChangeTitle', 'All is  God ');
    }
  },

}
</script>

<style scoped>
header{
    background: lightgreen;
    padding: 10px;
}
h1{
    color: #222;
    text-align: center;
}

</style>
