<template>
  <div>
    <h1>Named Slot</h1>
    <ChildComponent>
      <!-- Content injected into named slot -->
      <template v-slot:header>
        <h5>Header Content</h5>
        <p>
          This content will be injected into the header in the ChildComponent.
        </p>
      </template>
      <template v-slot:footer>
        <h5>Footer Content</h5>
        <p>
          This content will be injected into the footer in the ChildComponent.
        </p>
      </template>
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