<script>
export default {
  data() {
    return {
      inputText: '',
      displayText: '',
      showText: false,
      clickMessage: '',
    }
  },
  methods: {
    showText2() {
      this.displayText = this.inputText;
      this.inputText = '';
    },

    handleClick(event) {
      if (event.ctrlKey) {
        this.showText = true;
      } else {
        this.showText = false;
      }
    },
    handleLeftClick(event) {
      this.clickMessage = 'left';
    },

    handleMiddleClick() {
      this.clickMessage = 'middle';
    },

    handleRightClick() {
      this.clickMessage = 'right';
      return false; // Предотвращаем контекстное меню
    }
  }
}
</script>

<template>
  <div>
    <input
        type="text"
        v-model="inputText"
        @keyup.enter="showText2"
    >
    <p v-if="displayText">Вы ввели: <strong>{{ displayText }}</strong></p><br/>

    <a href="#" @click.prevent="handleClick">Кликните меня с зажатым Ctrl</a>
    <p v-if="showText">Вы нажали ссылку с зажатым Ctrl!</p><br/>

    <a
        href="#"
        @click.prevent="handleLeftClick"
        @click.middle.prevent="handleMiddleClick"
        @contextmenu.prevent="handleRightClick"
    >
      Кликните меня разными кнопками мыши
    </a>

    <p v-if="clickMessage">Нажата кнопка: <strong>{{ clickMessage }}</strong></p>
  </div>
</template>

<style>
div {
  margin: 50px;
}
</style>