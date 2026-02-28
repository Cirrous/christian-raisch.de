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
  width: 382px;
  max-height: 700px;
  margin: 74px 0;
}
</style>
