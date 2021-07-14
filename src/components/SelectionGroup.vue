<template>
  <div class="selection-group">
    <p class="title-group">{{ nameType }}</p>
    <OptionSelectionGroup
      v-for="(option, index) in detectData"
      :key="index"
      :value="option.value"
      :pathGrey="option.pathGrey"
      :pathGreen="option.pathGreen"
    />
    <img v-if="groupType == 'topics'" :src="iconAdd" @click="addTopic" />
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
          pathGrey: require("@/assets/icons/grey/candidate-profile.svg"),
          pathGreen: require("@/assets/icons/green/candidate-profile.svg"),
        },
        {
          value: "Propuesta Electoral",
          pathGrey: require("@/assets/icons/grey/candidate-workplan.svg"),
          pathGreen: require("@/assets/icons/green/candidate-workplan.svg"),
        },
        {
          value: "Contenido Extra",
          pathGrey: require("@/assets/icons/grey/candidate-media.svg"),
          pathGreen: require("@/assets/icons/green/candidate-media.svg"),
        },
        {
          value: "Foro",
          pathGrey: require("@/assets/icons/grey/candidate-foro.svg"),
          pathGreen: require("@/assets/icons/green/candidate-foro.svg"),
        },
      ],
      topics: [
        {
          value: "Educación",
          pathGrey: require("@/assets/icons/grey/topic-education.svg"),
          pathGreen: require("@/assets/icons/green/topic-education.svg"),
        },
        {
          value: "Medio Ambiente",
          pathGrey: require("@/assets/icons/grey/topic-enviroment.svg"),
          pathGreen: require("@/assets/icons/green/topic-enviroment.svg"),
        },
      ],
      iconAdd: require("@/assets/icons/green/event-add.svg"),
    };
  },
  computed: {
    detectData() {
      return this.$data[this.groupType];
    },
  },
  methods: {
    addTopic() {
      this.$data["topics"].push({
        value: "Economia",
        pathGrey: require("@/assets/icons/grey/topic-economy.svg"),
        pathGreen: require("@/assets/icons/green/topic-economy.svg"),
      });
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
  color: white;
}

img {
  border-radius: 50px;
  align-self: center;
  justify-self: center;
}

img:hover {
  background-color: #fff;
  padding: 2%;
}
</style>
