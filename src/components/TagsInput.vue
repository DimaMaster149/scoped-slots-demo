<template>
 <renderless-input :value="value" @input="(tags) => { $emit('input', tags) }">
    <div class="tags-input" slot-scope="{ tags, removeTag, inputAttrs, inputEvents }">
      <span class="tags-input-tag" v-for="(tag, index) in tags" :key="index">
        <span>{{ tag }}</span>
        <button type="button" class="tags-input-remove" @click="removeTag(tag)">&times;</button>
      </span>

      <input class="tags-input-text" placeholder="Add tag..." v-on="inputEvents" v-bind="inputAttrs">
    </div>
  </renderless-input>
</template>

<script>
import RenderlessInput from '@/components/RenderlessInput'
export default {
  props: ['value'],
  components: {
    RenderlessInput,
  }
}
</script>