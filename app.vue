<script setup lang="ts">
import { useRequestHeaders } from "#imports";
const headers = useRequestHeaders(["cookie"]);
const data = await $fetch("/temp.json", { headers });
console.log(JSON.stringify(data, null, 2));
</script>

<template>
  <div>data</div>
  <pre
    >{{ JSON.stringify(data, null, 2) }}
  </pre>
</template>
