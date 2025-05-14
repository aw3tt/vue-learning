<script>
export default {
  data() {
    return {
      text: '',
      words: [],
    }
  },
  methods: {
    splitText: function() {
      this.words = this.text
          .trim()
          .split(/\s+/)
          .filter(word => word.length > 0);
    }
  },
  computed: {

  }
}
</script>

<template>
  <textarea v-model="text"></textarea>
  <p>{{ text }}</p>

  <textarea v-model="text"></textarea>
  <button @click="splitText">Разделить на слова</button>
  <ul v-if="words.length > 0">
    <li v-for="(word, index) in words" :key="index">
      {{ word }}
    </li>
  </ul>
</template>

<style>

</style>