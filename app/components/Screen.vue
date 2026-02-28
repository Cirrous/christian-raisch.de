<template lang="pug">
.top_screen
  slot(name="top")

.bottom_screen
  slot(name="bottom")
</template>

<style>
.top_screen {
  height: 286px;
  background-image: url(@/assets/menu_grid_small.svg);
  background-size: contain;
}

.bottom_screen {
  margin-top: 151px;
  height: 286px;
  background-image: url(@/assets/menu_grid_large.svg);
  background-size: contain;
}
</style>
