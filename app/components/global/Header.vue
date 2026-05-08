<template lang="pug">
    .header
        img( class="header_bg" src="@/assets/header/header_bg.svg")
        .headerLeft
            p Chris
        .headerRight
            p(class="header_clock")
            p(class="header_date")
            img( class="header_icons" src="@/assets/header/header_icons.svg")
</template>

<style scoped>
.header {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 24px;
  width: 100%;
  color: var(--white);
}

.headerLeft,
.headerRight {
  z-index: 2;
  padding: 0 2px;
}

.headerLeft {
}

.header_bg {
  top: 0;
  position: absolute;
  height: 24px;
  padding-left: 2px;
  transform: scaleX(1.014);
}

.header_icons {
  height: 22px;
}
</style>
