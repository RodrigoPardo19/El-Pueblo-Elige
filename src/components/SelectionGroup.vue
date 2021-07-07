<template>
  <div class="selection-group">
    <p class="title-group">{{ nameType }}</p>
    <OptionSelectionGroup
      v-for="(option, index) in detectData"
      :key="index"
      :value="option.value"
      :path="option.path"
    />
  </div>
</template>

<script>
import OptionSelectionGroup from "@/components/Option.vue";

export default {
  name: "SelectionGroup",
  props: {
    nameType: String,
    groupType: String,
  },
  components: {
    OptionSelectionGroup,
  },
  data() {
    return {
      sections: [
        {
          value: "Perfil",
          path: require("@/assets/icons/candidate-profile.svg"),
        },
        {
          value: "Propuesta Electoral",
          path: require("@/assets/icons/candidate-workplan.svg"),
        },
        {
          value: "Contenido Extra",
          path: require("@/assets/icons/candidate-media.svg"),
        },
        { value: "Foro", path: require("@/assets/icons/candidate-foro.svg") },
      ],
      topics: [
        {
          value: "Educación",
          path: require("@/assets/icons/topic-education.svg"),
        },
        {
          value: "Medio Ambiente",
          path: require("@/assets/icons/topic-enviroment.svg"),
        },
      ],
    };
  },
  computed: {
    detectData() {
      return this.$data[this.groupType];
    },
  },
};
</script>

<style scoped>
.selection-group {
  display: grid;
  grid-template-columns: auto;
  grid-template-rows: repeat(5, 1fr);
}

.title-group {
  margin: 3%;
  margin-bottom: 1%;
  justify-self: start;
  align-self: end;
  font-size: small;
}
</style>
