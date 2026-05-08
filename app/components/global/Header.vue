<template lang="pug">
    .header
        img(class="header_bg" src="@/assets/header/header_bg.svg")
        .headerLeft
            p(class="header_user") Chris
        .headerRight
            ClientOnly
                p(class="header_clock") {{hours}}:{{minutes}}
                p(class="header_date") {{day}}/{{month}}
            img(class="header_icons" src="@/assets/header/header_icons.svg")
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";

const hours = ref("");
const minutes = ref("");
const day = ref("");
const month = ref("");

function updateTime() {
  const time = new Date();
  hours.value = time.getHours().toString().padStart(2, "0");
  minutes.value = time.getMinutes().toString().padStart(2, "0");
}

function updateDate() {
  const date = new Date();
  day.value = date.getDate().toString().padStart(2, "0");
  month.value = (date.getMonth() + 1).toString().padStart(2, "0");
}

let interval: ReturnType<typeof setInterval>;

onMounted(() => {
  updateTime();
  updateDate();
  interval = setInterval(updateTime, 1000);
});

onUnmounted(() => {
  clearInterval(interval);
});
</script>

<style scoped>
.header {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 24px;
  width: 100%;
  color: var(--white);
  line-height: 1.1;
  font-size: var(--xs);
}

.headerLeft,
.headerRight {
  z-index: 2;
  padding: 0 2px 3px 2px;
}

.headerRight {
  display: flex;
  margin-right: 71px;
  gap: 5px;
}

.header_bg {
  top: 0;
  position: absolute;
  height: 24px;
  padding-left: 2px;
  transform: scaleX(1.014);
}

.header_icons {
  top: -1px;
  right: 1px;
  position: absolute;
  height: 22px;
}

.header_clock,
.header_date,
.header_user {
  transform: scale(0.85);
}
</style>
