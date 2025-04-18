<!-- components/ToastUiEditor.vue -->
<template>
  <div ref="editor" class="tui-editor"></div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ToastUiEditor',
  async mounted() {
    const { default: Editor } = await import('@toast-ui/editor');
    const codeSyntaxHighlight = await import('@toast-ui/editor-plugin-code-syntax-highlight/dist/toastui-editor-plugin-code-syntax-highlight-all.js');

    new Editor({
      el: this.$refs.editor,
      initialValue: '',
      previewStyle: 'vertical',
      height: '300px',
      initialEditType: 'wysiwyg',
      plugins: [codeSyntaxHighlight.default],
    });
  },
});
</script>