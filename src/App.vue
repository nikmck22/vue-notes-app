<template>
	<div id="app">
    <toolbar />
    <button v-tooltip="'tooltip'">Click on Me</button>
    <v-popover>
      <button>Another button</button>
      <popButton slot="popover" />
    </v-popover>
    <note-container />
	</div>
</template>

<script>
import Toolbar from './components/Toolbar.vue'; 
import NoteContainer from './components/NoteContainer.vue';
import Vue from 'vue'
import VTooltip from 'v-tooltip'

Vue.use(VTooltip)

export default {
  name: 'app',
  components: {
    Toolbar,
    NoteContainer
  }
};


</script>

<style>
	/* RESET */
	* {
  margin: 0;
  padding: 0;
  border: 0;
  outline: none;
  box-sizing: border-box;
	}
	/* LAYOUT */
	#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
	}
	.toolbar {
  padding: 0.5em;
	}
	.toolbar-button, .toolbar-search {
  padding: inherit;
  border-radius: 0.3em;
	}
	.toolbar-search {
  float: right;
	}
	.note-container {
  display: flex;
  flex: 1;
	}
	.note-selectors {
  flex: 0 0 13em;
	}
	.note-selector {
  padding: 1em;
	}
	.note-selector p {
  margin: 0;
	}
	.note-editor {
  display: flex;
  flex: 1;
  flex-direction: column;
	}
	.note-editor-info {
  padding: 0.5em;
  text-align: center;
	}
	.note-editor-input {
  display: flex;
  flex: 1;
  width: 100%;
  padding: 0 2em 0 2em;
	}
	/* COLORS */
	* {
  color: #454545;
  background-color: #FAFAF8;
	}
	.toolbar {
  background-color: #DCDADC;
	}
	.toolbar-button {
  background-color: #FFFFFF;
	}
	.toolbar-button:active {
  background-color: #AAAAAA;
	}
	.note-selectors {
  border-right: 1px solid #DCDADC;
	}
	.note-selector {
  border-bottom: 1px solid #DCDADC;
	}
	.note-selector.active {
  background-color: #FCE18D;
	}
	.note-selector-title {
  background-color: inherit;
	}
	.note-selector-timestamp {
  color: #626262;
  background-color: inherit;
	}
	.note-editor-info {
  color: #DCDADC;
	}
	/* TYPOGRAPHY */
	body {
  font-family: sans-serif;
	}
	.note-selector-title {
  font-weight: bold;
	}
	.note-selector-timestamp {
  font-size: 0.7em;
	}
	.note-editor, .note-editor-input {
  font-size: 0.9em;
	}

.tooltip {
  display: block !important;
  z-index: 10000;
}

.tooltip .tooltip-inner {
  background: black;
  color: white;
  border-radius: 16px;
  padding: 5px 10px 4px;
}
/* 
.tooltip .tooltip-arrow {
  width: 0;
  height: 0;
  border-style: solid;
  position: absolute;
  margin: 5px;
  border-color: black;
  z-index: 1;
}

.tooltip[x-placement^="top"] {
  margin-bottom: 5px;
}

.tooltip[x-placement^="top"] .tooltip-arrow {
  border-width: 5px 5px 0 5px;
  border-left-color: transparent !important;
  border-right-color: transparent !important;
  border-bottom-color: transparent !important;
  bottom: -5px;
  left: calc(50% - 5px);
  margin-top: 0;
  margin-bottom: 0;
}

.tooltip[x-placement^="bottom"] {
  margin-top: 5px;
}

.tooltip[x-placement^="bottom"] .tooltip-arrow {
  border-width: 0 5px 5px 5px;
  border-left-color: transparent !important;
  border-right-color: transparent !important;
  border-top-color: transparent !important;
  top: -5px;
  left: calc(50% - 5px);
  margin-top: 0;
  margin-bottom: 0;
}

.tooltip[x-placement^="right"] {
  margin-left: 5px;
}

.tooltip[x-placement^="right"] .tooltip-arrow {
  border-width: 5px 5px 5px 0;
  border-left-color: transparent !important;
  border-top-color: transparent !important;
  border-bottom-color: transparent !important;
  left: -5px;
  top: calc(50% - 5px);
  margin-left: 0;
  margin-right: 0;
}

.tooltip[x-placement^="left"] {
  margin-right: 5px;
}

.tooltip[x-placement^="left"] .tooltip-arrow {
  border-width: 5px 0 5px 5px;
  border-top-color: transparent !important;
  border-right-color: transparent !important;
  border-bottom-color: transparent !important;
  right: -5px;
  top: calc(50% - 5px);
  margin-left: 0;
  margin-right: 0;
}

.tooltip.popover .popover-inner {
  background: #f9f9f9;
  color: black;
  padding: 24px;
  border-radius: 5px;
  box-shadow: 0 5px 30px rgba(black, .1);
}

.tooltip.popover .popover-arrow {
  border-color: #f9f9f9;
}

.tooltip[aria-hidden='true'] {
  visibility: hidden;
  opacity: 0;
  transition: opacity .15s, visibility .15s;
}

.tooltip[aria-hidden='false'] {
  visibility: visible;
  opacity: 1;
  transition: opacity .15s;
} */
	</style>