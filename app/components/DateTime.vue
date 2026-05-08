<template lang="pug">
    .datetime
            img(class="datetime_clock" src="@/assets/clock.svg")
            img(class="datetime_calendar" src="@/assets/calendar.svg")
</template>

<style scoped>
.datetime {
  margin-top: 24px;
  display: flex;
  justify-content: center;
  gap: 20px;
}

.datetime_clock,
.datetime_calendar {
  height: 146px;
}

.datetime_calendar {
  transform: scaleX(1.14);
}

.datetime_clock {
  margin-right: 18px;
}
</style>
