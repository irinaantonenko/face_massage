<template>
  <div>
    <h2>Current Temperature in Cities</h2>
    <ul>
      <li v-for="city in weatherData" :key="city.id">
        {{ city.name }}: {{ city.main.temp }}°C
      </li>
    </ul>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      weatherData: [],
    };
  },
  mounted() {
    this.getWeatherData();
  },
  methods: {
  getWeatherData() {
    const apikey = "1ada9e55428bb7900804e49efd0929a8";
    const cityIds = ["524901", "703448", "2643743"];
    const promises = [];

    cityIds.forEach((cityId) => {
      const promise = axios.get(
        `https://api.openweathermap.org/data/2.5/weather?id=${cityId}&units=metric&appid=${apikey}`
      );
      promises.push(promise);
    });

    Promise.all(promises)
      .then((responses) => {
        const data = responses.map((response) => response.data);
        this.weatherData = data;
      })
      .catch((error) => {
        console.log(error);
      });
  }
}
};
</script>
