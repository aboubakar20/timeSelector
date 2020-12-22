<template>
  <div>
    <h5>Avalable Weeks</h5>
    <div class="week">
      <div class="days">
        <input
          type="checkbox"
          id="sunday"
          value="Sunday"
          v-model="checkedDays"
        />
        <label for="sunday">Sunday</label>
      </div>
      <div class="days">
        <input
          type="checkbox"
          id="monday"
          value="Monday"
          v-model="checkedDays"
        />
        <label for="monday">Monday</label>
      </div>
      <div class="days">
        <input
          type="checkbox"
          id="tuesday"
          value="Tuesday"
          v-model="checkedDays"
        />
        <label for="tuesday">Tuesday</label>
      </div>
      <div class="days">
        <input
          type="checkbox"
          id="wednesday"
          value="Wednesday"
          v-model="checkedDays"
        />
        <label for="wednesday">Wednesday</label>
      </div>
      <div class="days">
        <input
          type="checkbox"
          id="thursday"
          value="Thursday"
          v-model="checkedDays"
        />
        <label for="thursday">Thursday</label>
      </div>
      <div class="days">
        <input
          type="checkbox"
          id="friday"
          value="Friday"
          v-model="checkedDays"
        />
        <label for="friday">Friday</label>
      </div>
      <div class="days">
        <input
          type="checkbox"
          id="saturday"
          value="Saturday"
          v-model="checkedDays"
        />
        <label for="saturday">Saturday</label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      checkedDays: [],
    };
  },
  updated() {
    console.log(this.checkedDays);
  },
};
</script>

<style scoped>
.week {
  padding: 30px;
  display: inline-flex;
  border: 1px solid;
}
.days {
  padding: 5px 10px;
}
</style>
