<template>
  <section class="container">
     <ckeditor v-model="editorData"></ckeditor>
  </section>
</template>

<script>
export default {
  name:'Editor',
  data(){
    return {
     editorData: '<p>Content of the editor.</p>'
      }
  }
}
</script>
