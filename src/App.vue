<template lang="">
  <!-- Header -->
  <div class="py-4 bg-green-500">
    <div class="container mx-auto">
      <!-- title -->
      <h6 class="text-xl md:text-3xl text-center text-white font-semibold font-mono">
        {{ data.title }}
      </h6>
    </div>
  </div>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      data: {
        title: 'Task List',
      },
    };
  },
};
</script>
<style lang=""></style>
