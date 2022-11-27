<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import LeftBar from "./components/LeftBar.vue";
import FixedMenuVue from "./components/FixedMenu.vue";
import LargeCardVue from "./components/LargeCard.vue";
import FriendActiveVue from "./components/FriendActive.vue";
</script>

<template>
  <div class="grid" id="main-grid">

    <div class="left-grid">
      <LeftBar />
    </div>

    <div class="mid-grid">

      <FixedMenuVue username="BasketballForce" />
      <h1 class="greeting">Good Afternoon</h1>

      <div class="large-card-contain">
        <LargeCardVue playlist="Liked Songs" image="heart.svg" class="bg-purp-white" />
        <LargeCardVue playlist="Baptized Imagination" image="kingk.jfif" />
        <LargeCardVue playlist="Poke & Chill" image="pokelofi.jpg" />
        <LargeCardVue playlist="Kings of Leon" image="kol.jpg" />
        <LargeCardVue playlist="Caamp" image="camp.jpg" />
        <LargeCardVue playlist="Cigarette Daydreams" image="cage.jfif" />
      </div>

    </div>

    <div class="right-grid">
      <FriendActiveVue profilepic="overcome.jpg" username="Bear Grylls" song="Survive" album="Overcome" artist="BearG"/>
    </div>

  </div>
</template>

<style scoped>
* {
  font-family: arial black;
  font-size: 13px;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 4fr 1fr;
  width: 100%;
  height: 100%
}

.left-grid,
.mid-grid,
.right-grid {
  display: inline-grid;
  background-color: red;
  grid-auto-rows: min-content;
  width: 100%;
  height: 100%;
}

.mid-grid {
  background: rgb(62, 62, 62);
  background: rgb(4,9,61);
  background: linear-gradient(180deg, rgba(4,9,61,1) 8%, rgb(2, 2, 29) 27%, rgb(12, 12, 12) 59%);
}

.right-grid {
  background-color: rgb(20, 20, 20);
}

.greeting {
  font-size: 2rem;
  color: white;
  margin-left: 2rem;
}

.large-card-contain{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  margin-left: 1rem;
}

</style>