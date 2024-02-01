<template>
    <div>
      <label for="city-input">Enter a city:</label>
      <vue-autosuggest
        id="city-input"
        :suggestions="suggestions"
        @input="getSuggestions"
        @selected="getWeather"
      >
        <template v-slot:default="{suggestion}">
          {{ suggestion.name }}
        </template>
      </vue-autosuggest>
      <div v-if="weather">
        <h2>{{ weather.name }}</h2>
        <p>Temperature: {{ weather.main.temp }}°C</p>
        <p>Conditions: {{ weather.weather[0].description }}</p>
      </div>
    </div>
  </template>
  
  <script>
  import VueAutosuggest from 'vue-autosuggest';
  import axios from 'axios';
  
  export default {
    name: 'WeatherApp',
    components: {
      VueAutosuggest,
    },
    data() {
      return {
        suggestions: [],
        weather: null,
      };
    },
    methods: {
      async getSuggestions(input) {
        const apiKey = '1ada9e55428bb7900804e49efd0929a8';
        const response = await axios.get(
          `https://api.openweathermap.org/data/2.5/find?q=${input}&units=metric&appid=${apiKey}`
        );
        this.suggestions = response.data.list;
      },
      async getWeather(suggestion) {
        const apiKey = '1ada9e55428bb7900804e49efd0929a8';
        const response = await axios.get(
          `https://api.openweathermap.org/data/2.5/weather?id=${suggestion.id}&units=metric&appid=${apiKey}`
        );
        this.weather = response.data;
      },
    },
  };
  </script>
  