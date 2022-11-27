<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import LeftBar from "./components/LeftBar.vue";
import FixedMenuVue from "./components/FixedMenu.vue";
import LargeCardVue from "./components/LargeCard.vue";
import FriendActiveVue from "./components/FriendActive.vue";
import SquareCardVue from "./components/SquareCard.vue";
import CategoryTitleVue from "./components/CategoryTitle.vue";
import FriendHeaderVue from "./components/FriendHeader.vue";
</script>

<template>
  <div class="grid" id="main-grid">

    <div class="left-grid">
      <LeftBar />
    </div>

    <div class="mid-grid">

      <FixedMenuVue username="BasketballForce" />
      <h1 class="greeting">Good <span id="time">Afternoon</span></h1>

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

      <CategoryTitleVue category="Recently Played"/>
      <div class="square-card-contain">
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Pokemon Lofi 🌸" image="pokemonLofi.jfif" artists_or_description="Best Pokemon Lofi hip hop mix - Chill beats to study, sleep, relax, chill to"/>
      <SquareCardVue playlist="Spongebob Ukulele Music" image="spongeuke.jfif" artists_or_description="you've been wanting to hear the full version of that one ukulele song from Spongebob? Well, (hopefully), you're in luck."/>
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
      <FriendHeaderVue/>
      <FriendActiveVue profilepic="overcome.jpg" username="Bear Grylls" song="Survive" album="Overcome" artist="BearG"/>
      <FriendActiveVue profilepic="overcome.jpg" username="Bear Grylls" song="Survive" album="Overcome" artist="BearG"/>
      <FriendActiveVue profilepic="overcome.jpg" username="Bear Grylls" song="Survive" album="Overcome" artist="BearG"/>

    </div>

  </div>
  <div class="player">f</div>
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
  height: 100%;
}

.left-grid,.mid-grid,.right-grid {
  display: inline-grid;
  background-color: red;
  grid-auto-rows: min-content;
  width: 100%;
  height: 90vh !important;
}

.mid-grid {
  background: rgb(4,9,61);
  background: linear-gradient(180deg, rgba(4,9,61,1) 8%, rgb(2, 2, 29) 27%, rgb(16, 16, 16) 59%);
  overflow-y: scroll;
  max-height: 100%;
}

.right-grid {
  background-color: rgb(20, 20, 20);
}

.greeting, #time {
  font-size: 1.75rem;
  color: white;
}
.greeting{
  margin-left: 2rem;
}

.large-card-contain{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  margin-left: 1rem;
}

.player{
  border-top: solid 2px rgb(48, 48, 48);
  height: 10%;
  position: fixed;
  width: 100%;
  top: 90%;
  background: #1a1a1a4a;
}

.square-card-contain{
  display: flex;
  flex-wrap: nowrap;
  margin-left: 1rem;
  max-width: 100%;
  overflow-y: hidden;
  margin-bottom: 1rem;
}

.square-card-contain::-webkit-scrollbar, .mid-grid::-webkit-scrollbar {
  width: .7em;
}
 
.square-card-contain::-webkit-scrollbar-thumb, .mid-grid::-webkit-scrollbar-thumb {
  background-color: rgb(44, 44, 44);
}

</style>

<script>
window.addEventListener('load', function () {
  var d = new Date();
var time = d.getHours();
var greeting = document.getElementById("time");

if (time >= 6 && time < 12 ) {
  greeting.innerText="Morning"
}
if (time >= 12 && time < 18) {
  greeting.innerText="Afternoon"
}
if (time >=18 || time < 6 ) {
  greeting.innerText="Evening";
}
})
</script>