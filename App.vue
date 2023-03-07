<template>
  
  <HelloWorld msg="Welcome to the for-loop:"/>
  
  <div id="app" v-for="event in events" :key="event.id">
    <p>
      ID : {{event.id }}
      <br/>
      Name: {{event.name}}
      <br/>
      Anzahl Teilnehmende : {{ event.participantCount }}
      </p>
</div>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  
  name: 'App',
  components: {
    HelloWorld
  },

  data(){
    return{
  events:[
    { id:1, name:'Veranstaltung1', participantCount : 7},
    { id:2, name:'Veranstaltung2', participantCount : 9},
    { id:3, name:'Veranstaltung3', participantCount : 13},
    { id:4, name:'Veranstaltung4', participantCount : 22},
  ],
 };
},

}


</script>

<style>
div { color : blue;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
