<template>
  <div>
    <h5>Avalable Weeks</h5>
    <div class="week">
      <div class="days" v-for="weekDay in weekDays" :key="weekDay.id">
        <input
          type="checkbox"
          :id="weekDay.day"
          :value="weekDay.day"
          v-model="checkedDays"
          @change="selectDays"
        />
        <label for="day">{{ weekDay.day }}</label>
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
  props: ["weekDays"],

  methods: {
    selectDays: function() {
      var sortDaysById = this.checkedDays.sort(function(a, b) {
        return parseInt(a.id) - parseInt(b.id);
      });
      this.$emit("selectedDays", sortDaysById);
    },
  },
};
</script>

<style scoped>
.week {
  border-radius: 5px;
  padding: 30px 150px;
  margin-bottom: 10px;
  display: flex;
  border: 1px solid;
}
.days {
  padding: 5px 10px;
}
</style>
