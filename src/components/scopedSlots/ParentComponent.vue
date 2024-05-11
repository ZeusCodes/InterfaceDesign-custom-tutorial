<template>
  <div>
    <h1>Scoped Slot</h1>
    <ChildComponent v-slot="{ message }">
      <!-- Accessing data passed from child component -->
      <p>Received message from child:{{ message }}</p>
    </ChildComponent>
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";

export default {
  components: {
    ChildComponent,
  },
};
</script>
