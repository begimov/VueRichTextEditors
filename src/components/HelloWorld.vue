<template>
  <div class="hello">
    <quillEditor :options="editorOption" v-model="content"></quillEditor>
  </div>
</template>

<script>
import 'quill/dist/quill.core.css'
import 'quill/dist/quill.snow.css'
import 'quill/dist/quill.bubble.css'

import { quillEditor } from 'vue-quill-editor'

export default {
  name: 'HelloWorld',
  components: {
    quillEditor
  },
  props: {
    msg: String
  },
  data () {
    return {
      content: '',
      editorOption: {
        modules: {
          toolbar: [['bold', 'italic'], [{ 'list': 'ordered'}, { 'list': 'bullet' }]]
        },
        placeholder: 'Compose an epic...1'
      },
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
