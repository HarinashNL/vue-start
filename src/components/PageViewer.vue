<template>
  <div v-if="page" class="container">
    <h1 class="emphasize">{{ page.pageTitle }}</h1>
    <p>{{ page.content }}</p>
  </div>
  <!-- <div v-else>
    <p>Loading...</p>
  </div> -->
</template>

<script>
export default {
  props:['index'],
  created() {
    this.page = this.$pages.getSinglePage(this.index);

    // this.$watch(() => this.$route.params, (newParams, prevPrams) => {
    //   this.page = this.$pages.getSinglePage(newParams.index);
    // })
  },
  data() {
    return {
      page: null,
    };
  },
  watch: {
    index(newIndex, oldIndex){
      this.page = this.$pages.getSinglePage(newIndex);
    }
  }
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
