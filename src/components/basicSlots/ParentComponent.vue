<template>
  <div>
    <h1>Basic Slot</h1>
    <ChildComponent>
      <!-- Content injected into default slot -->
      <p>This content will be injected into the slot in ChildComponent.</p>
    </ChildComponent>
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";
// @ is an alias to /src

export default {
  name: "ParentComponent",
  components: {
    ChildComponent,
  },
};
</script>