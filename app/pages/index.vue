<template lang="pug">
  Screen
    template(#top)
      Header
      h1 Top Content
      p Hier wird der Content für den oberen Screen angezeigt

    template(#bottom)
      h1 Bottom Content
      p Hier wird der Content für den unteren Screen angezeigt
</template>

<script lang="ts">
import Header from "~/components/global/Header.vue";
</script>
<style scoped></style>
