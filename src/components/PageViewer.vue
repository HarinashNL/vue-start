<template>
  <div class="container">
    <h1>{{ page.pageTitle }}</h1>
    <p>{{ page.content }}</p>
  </div>
  <!-- <div v-else>
    <p>Loading...</p>
  </div> -->
</template>

<script>
export default {
  props: ["page"],
};
</script>
