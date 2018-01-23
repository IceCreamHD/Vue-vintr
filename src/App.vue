<template>
  <div id="app">
    <blockquote v-on:click="displayQuote()">
      <p>{{currentQuote.content}}</p>
      <footer>
        — <cite>{{currentQuote.author}}</cite>
      </footer>
    </blockquote>
  </div>
</template>
<script>
export default {
  name: 'app',
  data () {
  return {
    currentQuote: {},
    quotes: [
      {
        content: "Бросайте дизайн",
        author: "Покрас Лампас"
      },
      {
        content: "Ты пидор",
        author: "Десигн"
      },
      {
        content: "Imma Savant",
        author: "Savant"
      }
    ]
  }
},
created: function() {
  this.displayQuote();
},
methods: {
  displayQuote: function(){
    var randomInt = Math.floor(Math.random() * (this.quotes.length - 0));
    this.currentQuote = this.quotes[randomInt];
  }
}
}
</script>
<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

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
