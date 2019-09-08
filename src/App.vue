<template>
  <div id="app">
    <tags-input v-model="tags" /> 
  </div>
</template>

<script>
import TagsInput from './components/TagsInput.vue'

export default {
  name: 'app',
  components: {
    TagsInput
  },
  data() {
    return {
      tags: []
    };
  },
}
</script>

<style>

</style>
