<!-- App.vue -->

// 🌀🌀💻 SCRIPT 💻🌀🌀
<script lang="ts">
import { defineComponent } from 'vue'
import AppFormComponent from '@/components/app-form/AppForm.component.vue'
// ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰
export default defineComponent({
  name: 'App',
  components: { AppFormComponent },
})
</script>
<!-- 🌀🌀💻================================================= -->

// 🌀🌀💻 HTML 💻🌀🌀
<template>
  <div class="formContainer">
    
    <!--⚫️ Will default to text, since no children were passed ⚫️-->
    <!--⚫️ Defaults if no children passed to the component ⚫️-->
    <h1>
      <span class="defaultText">
        <b>NO FORM TO RENDER</b>
      </span>
    </h1>
    
    <!--⚫️ BUTTON TEXT ⚫️-->
    <AppFormComponent>
      <!--⚫️ help-paragraph ⚫️-->
      <template v-slot:help>
        <p><b>This is some help text.</b></p>
      </template>

      <!--⚫️ fields-inputs ⚫️-->
      <template v-slot:fields>
        <input type="text" placeholder="email">
        <input type="text" placeholder="username">
        <input type="password" placeholder="password">
      </template>

      <!--⚫️ buttons ⚫️-->
      <template v-slot:buttons>
        <button type="submit" class="btnText">
          Submit
        </button>
      </template>
    </AppFormComponent>

    <!--⚫️ BUTTON CONTACT ⚫️-->
    <AppFormComponent>
      <!--⚫️ help-paragraph ⚫️-->
      <template v-slot:help>
        <p><b>Contact help text.</b></p>
      </template>

      <!--⚫️ fields-inputs ⚫️-->
      <template v-slot:fields>
        <input type="text" placeholder="name">
        <input type="text" placeholder="message">
      </template>

      <!--⚫️ buttons ⚫️-->
      <template v-slot:buttons>
        <button type="submit" class="btnsContacts">
          Submit
        </button>
      </template>
    </AppFormComponent>
    
  </div>
  
  
</template>
<!-- 🌀🌀💻================================================ -->

// 🌀🌀💻 STYLES 💻🌀🌀
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import 'src/components/app-form/StyledAppForm.scss';
/*⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰ */
//: - ∂
@mixin bgBlack() {
  position: absolute;
  width: 100%;
  min-height: 100%;
  left: 0;
  top: 0;
  background: #000;
}

@mixin alignContentCenter() {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1ch;
}

/*⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰ */
.formContainer {
  @include bgBlack;
  @include alignContentCenter;
  font-family: "Amazon Ember Cd RC", sans-serif;
  // ⚫️⚫️☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰☰
  h1 {
    font-family: "Amazon Ember Cd RC", sans-serif;
    color: white;
  }
}
</style>
<!-- 🌀🌀💻================================================ -->

