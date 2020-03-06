<template>
  <div>
    <h1>I am a blog post {{id}}</h1>
  </div>
</template>
<script>
export default {
  created() {
    console.log(this.$route.params.id);
    this.id = this.$route.params.id;
  },
  data: () => ({
    id: null
  })
};
</script>
