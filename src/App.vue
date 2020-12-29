<template>
  <div id="app">
    <h1>Time selector</h1>
    <WeekDaysSelector
      @selectedDays="getSelectedDays"
      :weekDays="weekDays"
    ></WeekDaysSelector>
  </div>
</template>

<script>
import WeekDaysSelector from "./components/WeekDaysSelector";
export default {
  name: "App",
  components: {
    WeekDaysSelector,
  },
  data() {
    return {
      weekDays: [
        {
          id: 0,
          day: "Sunday",
        },
        {
          id: 1,
          day: "Monday",
        },
        {
          id: 2,
          day: "Tuesday",
        },
        {
          id: 3,
          day: "Wednesday",
        },
        {
          id: 4,
          day: "Thursday",
        },
        { id: 5, day: "Friday" },
        {
          id: 6,
          day: "Saturday",
        },
      ],
      selectedDays: [],
    };
  },
  methods: {
    getSelectedDays: function() {
      this.selectedDays;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-left: 150px;
}
body {
  max-width: 1160px;
}
</style>
