<!-- FormComponent.vue -->

// 🌀🌀💻 SCRIPT 💻🌀🌀
<script lang="ts">
import { defineComponent } from 'vue'
// ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰
export default defineComponent({
  name: 'AppFormComponent',
})
</script>
<!-- 🌀🌀💻================================================= -->

// 🌀🌀💻 HTML 💻🌀🌀
<template>
  
  <form action="">
    
    <!--⚫️ Named slots ⚫️-->
    <div class="help">
      <slot name="help"></slot>
    </div>
    
    <div class="fields">
      <slot name="fields"></slot>
    </div>
    
    <div class="buttons">
      <slot name="buttons"></slot>
    </div>

    <!--⚫️ Able to have children | Will default in child components ⚫️-->
    <slot></slot>
  
  </form>
  
</template>
<!-- 🌀🌀💻================================================ -->

// 🌀🌀💻 STYLES 💻🌀🌀
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import 'StyledAppForm';
</style>
<!-- 🌀🌀💻================================================ -->

