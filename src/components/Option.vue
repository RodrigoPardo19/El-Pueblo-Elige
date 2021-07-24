<template>
  <div class="option">
    <div
      class="container"
      @mouseover="changeGreenIcon"
      @mouseleave="changeGreyIcon"
    >
      <img alt="IconOption" :src="path" />
      <a href=""> {{ value }} </a>
      <div v-if="editableOptions == 'true'" class="editableOptionsContainer">
        <img alt="IconDelete" :src="pathDelete" @click="deleteTopic" />
        <img alt="IconDrag" :src="pathDrag" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "OptionSelectionGroup",
  props: {
    value: String,
    pathGrey: String,
    pathGreen: String,
    pathDelete: String,
    pathDrag: String,
    editableOptions: Boolean,
  },
  data() {
    return {
      path: this.pathGrey,
    };
  },
  methods: {
    changeGreenIcon() {
      this.path = this.pathGreen;
    },
    changeGreyIcon() {
      this.path = this.pathGrey;
    },
    deleteTopic() {
      this.$emit("delete-topic");
    },
  },
};
</script>

<style scoped>
.option {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-content: center;
  margin-top: 0%;
  padding: 2%;
}

.container {
  display: flex;
  flex-direction: row;
  margin-left: 5%;
  margin-right: 5%;
  padding: 2%;
  border-radius: 5px;
  flex: 1;
}

.editableOptionsContainer {
  display: flex;
  margin-left: auto;
}

.editableOptionsContainer img {
  margin-left: 5px;
}

img {
  width: 19px;
  height: 19px;
  justify-self: center;
  align-self: center;
}

a {
  text-decoration: none;
  margin-left: 3%;
  margin-top: 5%;
  margin-bottom: 1%;
  color: #929dbd;
  font-size: 14px;
  font-weight: 500;
}

/* green: #34dba1 */
.container:hover {
  background-color: #fff;
}

.container:hover a {
  color: #11101b;
}
</style>
