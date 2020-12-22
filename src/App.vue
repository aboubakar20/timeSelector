<template>
  <div id="app">
    <h1>Time selector</h1>
    <WeekDaysSelector></WeekDaysSelector>
  </div>
</template>

<script>
import WeekDaysSelector from "./components/WeekDaysSelector";
export default {
  name: "App",
  components: {
    WeekDaysSelector,
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
  margin-top: 60px;
}
</style>
