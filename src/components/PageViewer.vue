<template>
  <div class="container">
    <h1 class="emphasize">{{ page.pageTitle }}</h1>
    <p>{{ page.content }}</p>
  </div>
  <!-- <div v-else>
    <p>Loading...</p>
  </div> -->
</template>

<script>
export default {
  created() {
    this.page = $this.$pages.getSinglePage(this.$route.params.index);
  },
  data() {
    return {
      page: null,
    };
  },
  // props: {
  //   page: {
  //     type: Object,
  //     default(rawProps) {
  //       return {
  //         pageTitle: "",
  //         content: "",
  //       };
  //     },
  //   },
  // },
};
</script>
<style scoped>
.emphasize {
  color: blue;
}
</style>
