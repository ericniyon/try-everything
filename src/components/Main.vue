<template>
<div id="country">
    <ul>
        <li v-for="country in countries" v-on:click="country.show = !country.show">
            <h3> {{  country.name }} </h3>
            <h4 v-show="country.show"> Capital city :{{  country.capital }} </h4>

        </li>
    </ul>
    <button v-on:click="DeleteCointry" >Delete</button>
</div>
</template>

<script>

export default {
    props:['countries'],
  data () {
    return {

    }
  },
  methods:{
      DeleteCointry:function(){
          this.countries.pop()
      }
  },

}
</script>

<style scoped>
#country{
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
}
ul{
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}
li{
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin:10px;

}
</style>
