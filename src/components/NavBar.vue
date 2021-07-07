<template>
  <nav class="nav-bar">
    <div class="container-start">
      <div class="container-icon-text">
        <img
          alt="Home Icon"
          src="../assets/icons/awesome-home.svg"
          class="nav-icon"
        />
        <a href="">Home</a>
      </div>
      <div class="container-icon-text">
        <img
          alt="Candidates Icon"
          src="../assets/icons/candidates.svg"
          class="nav-icon"
        />
        <a href="">Candidatos</a>
      </div>
    </div>
    <div class="container-center">
      <strong>El Pueblo Elige</strong>
    </div>
    <div class="container-end">
      <div class="container-icon-text">
        <img alt="User Icon" src="../assets/icons/user.svg" class="nav-icon" />
        <a href="">Profile</a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
nav {
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  grid-template-rows: 35px;
  border-bottom: solid 1px;
}

a {
  text-decoration: none;
  justify-self: center;
  align-self: center;
  margin-left: 4px;
  margin-top: 6px;
}

.nav-icon {
  height: 23px;
  width: 23px;
  justify-self: center;
  align-self: center;
}

.container-start {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  grid-column: 1/2;
}

.container-center {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-content: center;
  grid-column: 4/6;
}

.container-center > strong {
  justify-self: center;
  align-self: center;
}

.container-end {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-content: center;
  grid-column: 6/9;
  margin-right: 10px;
}

.container-end > a {
  justify-self: center;
  align-self: center;
}

.container-icon-text {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}
</style>
