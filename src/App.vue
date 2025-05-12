<script>
export default {
  data() {
    return {
      text: 'xxx'
    }
  },
  methods: {
    show: function(number) {
      alert(this.square(number));
    },
    change: function(text) {
      this.text = text;
    }
  }
}
</script>

<template>
  <p>{{ text }}</p>
  <button @click="change('yyy')">text</button>
  <button @click="change('zzz')">text2</button>
</template>
