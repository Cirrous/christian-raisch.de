<template lang="pug">
  Screen
    template(#top)
      Header
      DateTime

    template(#bottom)
      h1 Bottom Content
      p Hier wird der Content für den unteren Screen angezeigt
</template>

<script lang="ts">
import Header from "~/components/global/Header.vue";
import DateTime from "~/components/DateTime.vue";
</script>
<style scoped></style>
