<template>
  <div class="note-selector" v-on:click="setSelectedNote()" v-bind:class="{active: selectedNoteId === note.id}">
    <p class="note-selector-title">{{ note.body }}</p>
    <p class="note-selector-timestamp">Timestamp here...</p>
  </div>
</template>

<script>
export default {
  name: 'note-selector', 
  props: [
    "note", "selectedNoteId"
  ],

  methods: {
    setSelectedNote: function() {
      this.$emit("selectNote", this.note);
    }
  }
};
</script>