<template>
  <div class="cards">
    <div class="card" v-for="day in selectedDays" :key="day.id">
      <h3>{{ day.day }}</h3>
      <div class="text">
        <div class="col">
          <p>{{ time }}</p>
          <strong>Start Time</strong>
          <select>
            <option value="0">12:00 AM</option>
            <option value="1">1:00 AM</option>
            <option value="2">2:00 AM</option>
            <option value="3">3:00 AM</option>
            <option value="4">4:00 AM</option>
            <option value="5">5:00 AM</option>
            <option value="6">6:00 AM</option>
            <option value="7">7:00 AM</option>
            <option value="8">8:00 AM</option>
            <option value="9">9:00 AM</option>
            <option value="10">10:00 AM</option>
            <option value="11">11:00 AM</option>
            <option value="12">12:00 PM</option>
            <option value="13">1:00 PM</option>
            <option value="14">2:00 PM</option>
            <option value="15">3:00 PM</option>
            <option value="16">4:00 PM</option>
            <option value="17">5:00 PM</option>
            <option value="18">6:00 PM</option>
            <option value="19">7:00 PM</option>
            <option value="20">8:00 PM</option>
            <option value="21">9:00 PM</option>
            <option value="22">10:00 PM</option>
            <option value="23">11:00 PM</option>
          </select>
        </div>
        <div class="col ml-auto">
          <strong>End Time</strong>
          <select>
            <option value="0">12:00 AM</option>
            <option value="1">1:00 AM</option>
            <option value="2">2:00 AM</option>
            <option value="3">3:00 AM</option>
            <option value="4">4:00 AM</option>
            <option value="5">5:00 AM</option>
            <option value="6">6:00 AM</option>
            <option value="7">7:00 AM</option>
            <option value="8">8:00 AM</option>
            <option value="9">9:00 AM</option>
            <option value="10">10:00 AM</option>
            <option value="11">11:00 AM</option>
            <option value="12">12:00 PM</option>
            <option value="13">1:00 PM</option>
            <option value="14">2:00 PM</option>
            <option value="15">3:00 PM</option>
            <option value="16">4:00 PM</option>
            <option value="17">5:00 PM</option>
            <option value="18">6:00 PM</option>
            <option value="19">7:00 PM</option>
            <option value="20">8:00 PM</option>
            <option value="21">9:00 PM</option>
            <option value="22">10:00 PM</option>
            <option value="23">11:00 PM</option>
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
import moment from "moment";

export default {
  data() {
    return {
      time: null,
    };
  },
  props: ["selectedDays"],
  updated() {
    this.time = moment().format("hh mm A");
    console.log(this.time);
  },
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
