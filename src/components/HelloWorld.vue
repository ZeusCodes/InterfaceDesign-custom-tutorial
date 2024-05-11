<template>
  <div class="home">
    <ParentComponent></ParentComponent>
    <NamedParentComponent></NamedParentComponent>
    <ScopedParentComponent></ScopedParentComponent>
    <SMApp></SMApp>
  </div>
</template>

<script>
import ParentComponent from "./basicSlots/ParentComponent.vue";
import NamedParentComponent from "./namedSlots/ParentComponent.vue";
import ScopedParentComponent from "./scopedSlots/ParentComponent.vue";
import SMApp from "./SMApp.vue";
// @ is an alias to /src

export default {
  name: "HelloWorld",
  components: {
    ParentComponent,
    NamedParentComponent,
    ScopedParentComponent,
    SMApp,
  },
};
</script>