<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>And the time is {{ time }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      time: new Date().toLocaleTimeString(),
    };
  },
  mounted() {
    setInterval(() => {
      this.time = new Date().toLocaleTimeString();
    }, 1000);
  },
};
</script>
