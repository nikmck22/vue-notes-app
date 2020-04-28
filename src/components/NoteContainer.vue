<template>
  <div class="note-container">
      <note-selectors />
      <note-editor />
  </div>
</template>

<script>
import NoteEditor from './NoteEditor';
import NoteSelectors from './NoteSelectors';


export default {
  name: 'note-container',
  components: {
    NoteEditor,
    NoteSelectors
  }
};
</script>