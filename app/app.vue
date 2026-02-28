<template lang="pug">
  .shell
    .content
      NuxtLayout
        NuxtPage
</template>

<style>
.shell {
  display: flex;
  justify-content: center;
  width: 828px;
  height: 862px;
  background-image: url(@/assets/ds.svg);
}

.content {
  width: 384px;
  max-height: 700px;
  height: auto;
  margin: 68px 0 0px 0;
}
</style>
