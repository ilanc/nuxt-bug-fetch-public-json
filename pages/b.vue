<script setup lang="ts">
import { definePageMeta, useRequestHeaders } from "#imports";
definePageMeta({
  layout: "topnav",
});
const headers = useRequestHeaders(["cookie"]);
let data = await $fetch("/temp.json", { headers });
console.log(JSON.stringify(data, null, 2));
</script>

<template>
  <div>data</div>
  <pre
    >{{ JSON.stringify(data, null, 2) }}
  </pre>
</template>
