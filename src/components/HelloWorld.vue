<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 class="ess">Essential Links</h2>
    <button @click="startBaffleClick">ClickMe</button>
  </div>
</template>

<script>

import baffle from 'baffle';

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },

  mounted () {
    // on mounted property start obfuscating
    let b = baffle('.ess', {
    characters: '***********',
    speed: 150
    });
    b.reveal(5000);
  },
  methods:{

    // start the obfuscate
    startBaffleClick() {
       let b = baffle('.ess', {
        characters: '***********',
        speed: 150
        });

        // start 
        b.start();

        // reveal the  word
        b.reveal(1000)
        
    }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
</style>
