<template>
  <div class="subheading font-weight-regular">
    <p>"{{text}}"</p>
    <p v-show="author !== ''"> - {{author}}</p>
  </div>
</template>

<script>
export default {
  data: () => ({
    text: "",
    author: "",
    quotes: [
      { text: "Are you a parking ticket? because you've got fine written all over you.", },
      { text: "I like you just the way you are.", author: "Fred Rogers" },
      { text: "My interpretation can only be as inerrant as I am, and that's good to keep in mind.", author: "Rachel Held Evans"},
      { text: "So what did God say to me in the silence that morning? I’m not sure, but I think God said something like, Don’t try so hard, little child, and, Hey, check out this cool turtle I made.", author: "Rachel Held Evans"},
      { text: "When I was a boy, I would lay in my twin sized bed and wonder where my brother was.", author: "Mitch Hedberg"},
      { text: "I saw this wino who was eating grapes. It's like, 'Dude, you have to wait.'", author: "Mitch Hedberg"},
      { text: "I Nelope!", author: "P"},
      { text: "I right here!", author: "P"},
      // { text: "", author: ""},
      // { text: "", author: ""},
      // { text: "", author: ""},
      // { text: "", author: ""},
      // { text: "", author: ""},
      // { text: "", author: ""},
    ]
  }),
  mounted: function() {
    const self = this;
    self.setRandomQuote();
  },
  methods: {
    getRandomQuoteIndex: function() {
      const self = this;
      var max = self.quotes.length;
      return Math.floor(Math.random() * max);
    },
    getRandomQuote: function() {
      const self = this;
      return self.quotes[self.getRandomQuoteIndex()];
    },
    setRandomQuote: function() {
      const self = this;

      var quote = self.getRandomQuote();
      self.text = quote.text;
      if (quote.author !== undefined) {
        self.author = quote.author;
      } else {
        self.author = "";
      }
    }
  }
};
</script>