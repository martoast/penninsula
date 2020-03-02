<template>
  <div>
    <h1>I am a blog post {id}</h1>
  </div>
</template>
<script>
export default {
  data: () => ({ id: this.$route.params.id })
};
</script>
