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
  font-family: "Times New Roman";
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
  font-size: 50px;
  margin-left: 40px;
}
.back-button {
  height: 70%;
  width: auto;
  margin-right: 40px;
}
</style>
