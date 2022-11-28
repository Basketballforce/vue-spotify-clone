<script setup></script>

<template>
  <div class="friend-header">
    <p class="friend-activity">Friend Activity</p>
    <div>
      <img class="icon-spacer" src="../assets/user-plus.svg" alt="" />
      <img class="icon-spacer" id="close-friend" src="../assets/x.svg" alt="" />
    </div>
  </div>
</template>

<style scoped>
.friend-activity {
  margin-top: 2rem;
  margin-left: 1rem;
  font-size: 1rem;
}

.friend-header {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}

.icon-spacer {
  margin-right: 1rem;
  filter: brightness(0.5);
  cursor: pointer;
}

.icon-spacer:hover {
  filter: brightness(1);
}
</style>

<script>
window.addEventListener("load", function () {
  const rightGrid = document.getElementById("friend-grid");
  const closefriend = document.getElementById("close-friend");

  closefriend.addEventListener("click", closeFriendPane);

  function closeFriendPane() {
    rightGrid.style.display = "none";
    changeFixedElementWidth();
  }
});
</script>
