<template>
  <div class="header">
    <div class="content-wrapper">
      <span class="header-title">NEWS</span>
      <img class="back-button" src="../assets/back-button.png" />
    </div>
  </div>
</template>
<style scoped>
.header {
  font-family: 'Times New Roman';
  width: 100%;
  height: 80px;
  display: flex;
  align-items: center;
  background-color: blueviolet;
}
.content-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 3px double rgb(255, 255, 255);
  width: 100%;
  height: 80%;
}
.header-title {
  font-size: min(7vw, 50px);
  margin-left: min(7vw, 40px);
}
.back-button {
  height: min(7vw, 70%);
  width: auto;
  margin-right: min(7vw, 40px);
}
</style>
