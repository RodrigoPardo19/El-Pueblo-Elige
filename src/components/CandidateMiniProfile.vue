<template>
  <div class="candidate-mini-profile">
    <img
      alt="Candidate-Photo"
      src="../assets/icons/user-photos/candidate-photo.svg"
      class="photo"
    />
    <Strong>Rodrigo Alexis Pardo Gatica</Strong>
    <p>Candidato a Presidente de la Republica</p>
  </div>
</template>

<script>
export default {
  name: "CandidateMiniProfile",
};
</script>

<style scoped>
.candidate-mini-profile {
  display: flex;
  flex-direction: column;
}

.photo {
  padding-top: 10%;
  padding-left: 20%;
  padding-right: 20%;
  padding-bottom: 5%;
}

strong {
  color: #929dbd;
  font-size: smaller;
}

p {
  margin: 0px;
  margin-top: 2%;
  font-size: small;
  color: #929dbd;
}
</style>
