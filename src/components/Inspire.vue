<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div>
      <button @click="generate" class="inspireButton">
        How about some wisdom
      </button>
      <div class="flex-container" mt-3>
        <div class="quote">{{ quote.quote }}</div>
        <div class="quoter">{{ quote.cite }}</div>
      </div>
    </div>
  </div>
</template>

<script>
const quotes = [
  {
    quote:
      "One of my most productive days was throwing away 1,000 lines of code.",
    cite: "Ken Thompson",
  },
  {
    quote:
      "I have always wished for my computer to be as easy to use as my telephone; my wish has come true because I can no longer figure out how to use my telephone.",
    cite: "Bjarne Stroustrup",
  },
  {
    quote: "When in doubt, use brute force.",
    cite: "Floor Schouten",
  },
];
export default {
  name: "Inspire",
  props: {
    msg: String,
  },
  data() {
    return { quote: {} };
  },
  methods: {
    generate() {
      const index = Math.floor(Math.random() * quotes.length);
      this.quote = quotes[index];
    },
  },
};
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
.flex-container {
  margin: 20px;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.quote {
  margin-bottom: 10px;
  max-height: 100px;
  max-width: 350px;
}
.quoter {
  max-height: 100px;
}
.inspireButton {
  border: 3px solid coral;
  height: 40px;
  background-color: white;
  transition: background-color 1s ease-out 100ms;
}
.inspireButton:hover {
  background-color: rgb(248, 197, 197);
  box-shadow: 5px 5px coral;
}
.inspireButton:active {
  box-shadow: -2px -2px #000;
}
</style>
