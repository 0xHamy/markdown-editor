<!-- pages/index.vue -->
<template>
  <div>
    <h1>Markdown Editor</h1>
    <ClientOnly>
      <ToastUiEditor />
    </ClientOnly>
  </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
});
</script>

<style>
.tui-editor {
  border: 1px solid #ccc;
  padding: 10px;
  min-height: 300px;
}
</style>