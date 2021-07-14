<template>
  <div class="option">
    <div class="container">
      <img alt="IconOption" :src="pathGrey" />
      <a href=""> {{ value }} </a>
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
  },
  data() {
    return {
      url: this.pathGreen,
    };
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
  align-content: center;
  margin-left: 5%;
  margin-right: 5%;
  padding: 2%;
  border-radius: 5px;
  flex: 1;
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

.container:hover img {
  background-image: v-bind(url);
}
</style>
