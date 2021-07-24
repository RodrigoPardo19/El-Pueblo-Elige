<template>
  <div class="editor">
    <editor-menu-bar :editor="editor" v-slot="{ commands, isActive }">
      <div class="menubar">
        <button
          class="menubar__button"
          :class="{ 'is-active': isActive.bold() }"
          @click="commands.bold"
        >
          Negrita
        </button>
        <button
          class="menubar__button"
          :class="{
            'is-active': isActive.customstyle({ level: 'body-green' }),
          }"
          @click="commands.customstyle({ level: 'body-green' })"
        >
          Verde
        </button>
        <button
          class="menubar__button"
          :class="{ 'is-active': isActive.customstyle({ level: 'body-blue' }) }"
          @click="commands.customstyle({ level: 'body-blue' })"
        >
          Azul
        </button>
        <button
          class="menubar__button"
          :class="{ 'is-active': isActive.customstyle({ level: 'body-red' }) }"
          @click="commands.customstyle({ level: 'body-red' })"
        >
          Rojo
        </button>
        <button
          class="menubar__button"
          :class="{ 'is-active': isActive.italic() }"
          @click="commands.italic"
        >
          Cursiva
        </button>
        <button
          class="menubar__button"
          :class="{ 'is-active': isActive.heading({ level: 1 }) }"
          @click="commands.heading({ level: 1 })"
        >
          Título 1
        </button>
        <button
          class="menubar__button"
          :class="{ 'is-active': isActive.heading({ level: 2 }) }"
          @click="commands.heading({ level: 2 })"
        >
          Título 2
        </button>
        <button
          class="menubar__button"
          :class="{ 'is-active': isActive.heading({ level: 3 }) }"
          @click="commands.heading({ level: 3 })"
        >
          Título 3
        </button>
      </div>
    </editor-menu-bar>

    <editor-content
      class="editor__content"
      style="background: rgba(100, 100, 0, 0.2)"
      :editor="editor"
    />

    <pre>{{ localHTML }}</pre>
    <pre>{{ localJSON }}</pre>
  </div>
</template>

<script>
import { Editor, EditorContent, EditorMenuBar } from "tiptap";
import {
  Blockquote,
  Bold,
  BulletList,
  Code,
  CodeBlock,
  HardBreak,
  Heading,
  History,
  HorizontalRule,
  Italic,
  Link,
  ListItem,
  OrderedList,
  Strike,
  TodoItem,
  TodoList,
  Underline,
} from "tiptap-extensions";
import CustomStyle from "./CustomStyle";
//import RealtimeExtension from "./Realtime";

export default {
  components: {
    EditorContent,
    EditorMenuBar,
  },
  data() {
    return {
      localJSON: "",
      localHTML: "",
      editor: new Editor({
        extensions: [
          new Blockquote(),
          new BulletList(),
          new CodeBlock(),
          new HardBreak(),
          new Heading({ levels: [1, 2, 3] }),
          new HorizontalRule(),
          new ListItem(),
          new OrderedList(),
          new TodoItem(),
          new TodoList(),
          new Link(),
          new Bold(),
          new Code(),
          new Italic(),
          new Strike(),
          new Underline(),
          new History(),
          //new RealtimeExtension(),
          new CustomStyle(),
        ],

        content: ``,
      }),
    };
  },
  beforeDestroy() {
    this.editor.destroy();
  },
};
</script>

<style>
.menubar__button {
  font-weight: 700;
  display: -webkit-inline-box;
  display: -ms-inline-flexbox;
  display: inline-flex;
  background: rgba(0, 0, 0, 0);
  border: 0;
  color: #000;
  padding: 0.2rem 0.5rem;
  margin-right: 0.2rem;
  border-radius: 3px;
  cursor: pointer;
}
.menubar__button:hover {
  background-color: rgba(0, 0, 0, 0.05);
}
.menubar__button.is-active {
  background-color: rgba(0, 0, 0, 0.1);
}
pre {
  white-space: pre-wrap; /* Since CSS 2.1 */
  white-space: -moz-pre-wrap; /* Mozilla, since 1999 */
  white-space: -pre-wrap; /* Opera 4-6 */
  white-space: -o-pre-wrap; /* Opera 7 */
  word-wrap: break-word; /* Internet Explorer 5.5+ */
}

.body-blue {
  color: blue;
}
.body-red {
  color: red;
}
.body-green {
  color: green;
}
</style>