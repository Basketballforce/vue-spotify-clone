<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import LeftBar from "./components/LeftBar.vue";
import FixedMenuVue from "./components/FixedMenu.vue";
import LargeCardVue from "./components/LargeCard.vue";
import FriendActiveVue from "./components/FriendActive.vue";
import SquareCardVue from "./components/SquareCard.vue";
import CategoryTitleVue from "./components/CategoryTitle.vue";
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
      
      
      <CategoryTitleVue category="Recently Played"/>
      <div class="square-card-contain">
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Spongebob Ukulele Music" image="spongeuke.jfif" artists_or_description="you've been wanting to hear the full version of that one ukulele song from Spongebob? Well, (hopefully), you're in luck."/>
      </div>
      

    </div>

    <div class="right-grid">
      <FriendActiveVue profilepic="overcome.jpg" username="Bear Grylls" song="Survive" album="Overcome" artist="BearG"/>
    </div>

  </div>
  <div class="player"></div>
</template>

<style scoped>
* {
  font-family: arial black;
  font-size: 13px;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 5fr 1.25fr;
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
  background: rgb(4,9,61);
  background: linear-gradient(180deg, rgba(4,9,61,1) 8%, rgb(2, 2, 29) 27%, rgb(12, 12, 12) 59%);
}

.right-grid {
  background-color: rgb(20, 20, 20);
}

.greeting {
  font-size: 1.75rem;
  color: white;
  margin-left: 2rem;
}

.large-card-contain{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  margin-left: 1rem;
}

.player{
  border-top: solid 1px rgb(48, 48, 48);
}

.square-card-contain{
  display: flex;
  flex-wrap: nowrap;
  margin-left: 1rem;
  max-width: 100%;
  overflow-y: hidden;
}

</style>