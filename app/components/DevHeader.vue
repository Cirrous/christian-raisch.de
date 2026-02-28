<template lang="pug">
  div
    nav
      ul
        li
          NuxtLink(to="/") Home
        li
          NuxtLink(to="/leaderline") LeaderLine
        li
          NuxtLink(to="/components") Components
</template>

<style scoped>
nav {
  display: block;
}

ul {
  display: flex;
  flex-direction: row;
  gap: 40px;
  margin: unset;
}

div {
  border: 1px solid red;
}
</style>
