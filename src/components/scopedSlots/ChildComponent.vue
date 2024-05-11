<template>
  <div>
    <!-- Passing data to parent component using scoped slot -->
    <slot :message="childMessage"></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      childMessage: "Hello from child!",
    };
  },
};
</script>
