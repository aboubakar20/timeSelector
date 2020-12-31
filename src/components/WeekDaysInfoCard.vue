<template>
  <div class="cards">
    <div class="card" v-for="day in selectedDays" :key="day.id">
      <h3>{{ day.day }}</h3>
      <div class="text">
        <div class="col">
          <strong>Start Time</strong>
          <select>
            <option
              v-for="startTime in timeSlot"
              :key="'startTime' + startTime.value"
              >{{ startTime.time }}</option
            >
          </select>
        </div>
        <div class="col ml-auto">
          <strong>End Time</strong>
          <select>
            <option
              v-for="endTime in timeSlot"
              :key="'endTime' + endTime.value"
              >{{ endTime.time }}</option
            >
          </select>
          <div class="btn">
            <button>Add Time</button>
          </div>
        </div>
      </div>
      <ul>
        <li>
          <span>01:00 AM - 02:00 AM</span>
          <em>x</em>
        </li>
        <li>
          <span>01:00 AM - 02:00 AM</span>
          <em>x</em>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
// import moment from "moment";

export default {
  data() {
    return {
      timeSlot: [
        { value: "0", time: "12:00 AM" },
        { value: "1", time: "01:00 AM" },
        { value: "2", time: "02:00 AM" },
        { value: "3", time: "03:00 AM" },
        { value: "4", time: "04:00 AM" },
        { value: "5", time: "05:00 AM" },
        { value: "6", time: "06:00 AM" },
        { value: "7", time: "07:00 AM" },
        { value: "8", time: "08:00 AM" },
        { value: "9", time: "09:00 AM" },
        { value: "10", time: "10:00 AM" },
        { value: "11", time: "11:00 AM" },
        { value: "12", time: "12:00 PM" },
        { value: "13", time: "01:00 PM" },
        { value: "14", time: "02:00 PM" },
        { value: "15", time: "03:00 PM" },
        { value: "16", time: "04:00 PM" },
        { value: "17", time: "05:00 PM" },
        { value: "18", time: "06:00 PM" },
        { value: "19", time: "07:00 PM" },
        { value: "20", time: "08:00 PM" },
        { value: "21", time: "09:00 PM" },
        { value: "22", time: "10:00 PM" },
        { value: "23", time: "11:00 PM" },
      ],
    };
  },
  props: ["selectedDays"],
};
</script>

<style scoped>
* {
  box-sizing: border-box;
}
.cards {
  letter-spacing: -5px;
  margin: 0 -5px;
  text-align: left;
}
.cards * {
  letter-spacing: 0;
}
ul {
  padding: 0 5px;
}
ul li {
  display: flex;
  margin: 0 0 15px;
}
ul em {
  margin-left: auto;
  font-style: normal;
}
ul span {
  max-width: 80%;
}
.card {
  border-radius: 5px;
  border: 1px solid;
  margin: 0 5px 10px;
  padding: 5px 20px;
  display: inline-block;
  vertical-align: top;
  width: 49%;
}
h3 {
  margin: 0 0 10px;
}
.text {
  display: flex;
  padding: 10px;
  background: #eaeaea;
  border-top: 1px solid #d0cece;
  border-bottom: 1px solid #d0cece;
  border-radius: 5px;
}
.text .col {
  flex-grow: 1;
  padding-right: 10px;
}
.text strong {
  display: block;
  font-size: 15px;
  color: #969696;
  margin: 0 0 6px;
}
.text select {
  width: 100%;
  display: block;
  height: 27px;
}
.btn {
  overflow: hidden;
  text-align: right;
  padding: 11px 0 0;
}
</style>
