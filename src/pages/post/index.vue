<script setup>
    import Editor from '@tinymce/tinymce-vue'
    const content = ref("")

    const getContent = () => {
      const editor = tinymce.activeEditor
      const contentHtml = editor.getContent()
      content.value = contentHtml
      console.log(content.value) // or do whatever you want with the contentHtml
    }



</script>

<template>
  <div v-motion-fade >
    <div class="text-center font-bold text-3xl mt-4 text-slate-900 dark:text-white">Post </div>
   
        <div id="app">
  <editor
    api-key="jkrr4gz3kdl4u12jucwzhhhob8werj7rm4j3z2ka35c2qvbh"
    :init="{
      height: 500,
      menubar: false,
      plugins: [
        'a11ychecker','advlist','advcode','advtable','autolink','checklist','export',
        'lists','link','image','charmap','preview','anchor','searchreplace','visualblocks',
        'powerpaste','fullscreen','formatpainter','insertdatetime','media','table','help','wordcount'
      ],
      toolbar:
        'undo redo | casechange blocks | bold italic backcolor | \
        alignleft aligncenter alignright alignjustify | \
        bullist numlst checklist outdent indent | removeformat | a11ycheck code table media image help'
    }"
    v-model:content="content"
    id="myEditor"
  />
  <div class="flex flex-row justify-center mb-11 mt-8">
 <v-btn @click = "getContent"
 color="blue" size="large" rounded="pill">
  <p class="font-bold"> Preview</p>
 </v-btn>
</div>
<div v-html="content"></div>
</div>
</div>

</template>

<style scoped>

</style>
