<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>The current time is {{ timestamp.toLocaleString() }}</p>
  </div>
</template>

<script>
export default {
  name: "About",

  data() {
    return {
      timestamp: null,
    };
  },

  mounted() {
    this.startClock();
  },

  methods: {
    startClock() {
      setInterval(() => {
        this.timestamp = new Date();
      }, 1000);
    },
  },
};
</script>
