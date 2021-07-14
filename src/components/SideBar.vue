<template>
  <div class="side-bar">
    <CandidateMiniProfile />
    <SelectionGroup nameType="Secciones" groupType="sections" />
    <SelectionGroup nameType="Tópicos" groupType="topics" />
  </div>
</template>

<script>
import SelectionGroup from "@/components/SelectionGroup.vue";
import CandidateMiniProfile from "@/components/CandidateMiniProfile.vue";

export default {
  name: "SideBar",
  components: {
    SelectionGroup,
    CandidateMiniProfile,
  },
};
</script>

<style scoped>
.side-bar {
  background-color: #11101b;
  width: 255px;
  height: 930px;
  border-right: solid 1px;
}
</style>
