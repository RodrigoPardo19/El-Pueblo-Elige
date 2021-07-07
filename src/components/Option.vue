<template>
  <div class="option">
    <div class="container">
      <img alt="IconOption" :src="path" />
      <a href=""> {{ value }} </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "OptionSelectionGroup",
  props: {
    value: String,
    path: String,
  },
};
</script>

<style scoped>
.option {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-content: center;
  border: solid 1px;
  margin-top: 0%;
  margin-left: 4%;
  margin-right: 4%;
  margin-bottom: 2%;
  padding: 2%;
}

.container {
  display: flex;
  flex-direction: row;
  align-content: center;
  margin-left: 5%;
  margin-right: 5%;
  flex: 1;
}

img {
  width: 20px;
  height: 20px;
  justify-self: center;
  align-self: center;
}

a {
  text-decoration: none;
  margin-left: 3%;
  margin-top: 5%;
  margin-bottom: 1%;
}
</style>
