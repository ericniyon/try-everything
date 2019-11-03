<template>
  <div>
    <app-header v-bind:title='title' v-on:ChangeTitle="updateTitle($event)"></app-header>
    <app-main v-bind:countries='countries'></app-main>
    <app-footer v-bind:title="title"></app-footer>

  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Main from './components/Main.vue';


export default {
  components:{
    'app-header': Header,
    'app-footer': Footer,
    'app-main': Main
},

  data () {
    return {
      countries:[
            {name:'Rwanda', capital:'Kigali', show:false},
            {name:'Uganda', capital:'Kampala', show:false},
            {name:'Kenya', capital:'Nairobi', show:false},
            {name:'Tanzania', capital:'Dodoma', show:false},
            {name:'R.D.C', capital:'Kinshasa', show:false},
            {name:'Burundi', capital:'Bujumbura', show:false},
            {name:'Angola', capital:'Free town', show:false},
            {name:'Nigeria', capital:'Nigeri', show:false},


        ],

        title:'Vue Application'
      
    }
  },
  methods:{
    updateTitle:function(updatedTitle){
      this.title = updatedTitle;
    }
  },

}
</script>

<style >

</style>
