<script setup>
const props = defineProps({
  msg: {
    type: String,
    required: true,
  },
  icon: {
    type: String,
    required: true,
  },
});

function getimage() {
  return new URL(`../assets/${props.icon}`, import.meta.url);
}
</script>

<template>
  <div class="left-bar-menu">
    <img :src="getimage()" alt="menu-item" class="menu-item" />
    <h3>{{ msg }}</h3>
  </div>
</template>

<style scoped>
.left-bar-menu {
  padding-top: 0.5rem;
  background-color: black;
  display: grid;
  grid-template-columns: 0.25fr 1fr;
  align-items: center;
  padding-right: 1rem;
  grid-gap: 10px;
  padding-bottom: 1rem;
}
.menu-item {
  width: 40px;
}
header {
  display: inline;
}

.selected > h3 {
  font-weight: bold;
  color: white;
}

h3 {
  white-space: nowrap;
}

.selected > img {
  filter: brightness(1);
}

img {
  filter: brightness(0.5);
}

img:hover {
  filter: brightness(1);
}

h3:hover {
  color: white;
}

* {
  transition: 0.5s;
}

*:hover {
  cursor: pointer;
}

.bg-light-grey > img {
  background-color: lightgrey;
  border-radius: 5px;
  padding: 0.45rem;
}

.hover-group:hover > img {
  filter: brightness(1);
  color: white;
}
.hover-group:hover > h3 {
  color: white;
}

.bg-purp-white > img {
  padding: 0.6rem;
  filter: blur(0.5);
  background: rgb(50, 22, 149);
  background: linear-gradient(
    133deg,
    rgba(50, 22, 149, 1) 10%,
    rgba(84, 53, 207, 1) 47%,
    rgba(199, 235, 255, 1) 92%
  );
  border-radius: 5px;
}
</style>
