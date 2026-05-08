<template lang="pug">
.top_screen
  slot(name="top")

.bottom_screen
  slot(name="bottom")
</template>

<style>
.top_screen,
.bottom_screen {
  height: 286px;
  background-size: contain;
}
.top_screen {
  background-image: url(@/assets/menu_grid_small.svg);
}

.bottom_screen {
  margin-top: 151px;
  background-image: url(@/assets/menu_grid_large.svg);
}
</style>
