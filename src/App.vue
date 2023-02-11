<template>
  <div class="app">
    <AppHeader title="The Anime Quoter"/>
    <Quote v-for="quote in quotes" 
    :key="quote.id"
    :content="quote.content"
    :author="quote.author"
    :category="quote.category"
    :avtar_img="quote.avtar_img"  />
    <div class="button-container">
      <button @click="getQuote">Generate</button>
    </div>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import Quote from './components/Quote.vue';
import JsonQuotes from "./json/quotes.json";

export default {
  name: 'App',
  components: {
    AppHeader,
    Quote,

  },
  data() {
      return {
        quotes: JsonQuotes
    }
  }
}
</script>

<style lang="scss">
  :root {
    --primary: #d81e5b;
    --scondary: #2c3e5b;
    --dark: #131a26;
    --light: #eee;
    --grey: #848484;
  }
  * {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    margin: 0;
    padding: 0;
  }
  body {
    background-color: var(--dark);
  }
  .button-container {
    display: flex;
    justify-content: center;

    button {
      border: none;
      outline: none;
      background-color: var(--primary);
      padding: 16px 32px;
      border-radius: 99px;
      color: var(--light);
      font-size: 28px;
      font-weight: 700;
      text-transform: uppercase;
      cursor: pointer;
      transition: 0.4s;

        &:hover {
          background-color: var(--scondary);
        }
      }
  }
</style>