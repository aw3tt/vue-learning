<script>
export default {
  data() {
    return {
      choice: '',
      selectedLanguage: '',
    }
  },
  methods: {

  },
  computed: {

  }
}
</script>

<template>
  <div>
    <label>
      <input name="language" type="radio" v-model="choice" value="Русский">
      Русский
    </label><br>

    <label>
      <input name="language" type="radio" v-model="choice" value="Английский">
      Английский
    </label><br>

    <label>
      <input name="language" type="radio" v-model="choice" value="Французский">
      Французский
    </label><br>

    <p>Вы выбрали: <strong>{{ choice || 'язык не выбран' }}</strong></p>
  </div>

  <div>
    <h3>Выберите ваш родной язык:</h3>

    <label>
      <input name="language" type="radio" v-model="selectedLanguage" value="ru">
      Русский
    </label><br>

    <label>
      <input name="language" type="radio" v-model="selectedLanguage" value="en">
      English
    </label><br>

    <label>
      <input name="language" type="radio" v-model="selectedLanguage" value="fr">
      Français
    </label><br>

    <div>
      <p v-if="selectedLanguage === 'ru'">
        Добро пожаловать! Мы рады видеть вас на нашем сайте.
      </p>

      <p v-if="selectedLanguage === 'en'">
        Welcome! We're glad to see you on our website.
      </p>

      <p v-if="selectedLanguage === 'fr'">
        Bienvenue ! Nous sommes heureux de vous voir sur notre site.
      </p>

      <p v-if="!selectedLanguage" class="hint">
        Пожалуйста, выберите язык для отображения приветствия
      </p>
    </div>
  </div>
</template>

<style>

</style>