<script setup>import LeftMenuItemVue from './LeftMenuItem.vue';
import LeftMenuPlaylistVue from './LeftMenuPlaylist.vue';
</script>

<template>
  <div class="left-bar">
    <img src="./../assets/more-horizontal.svg" alt="dot-menu" class="dot-menu">
    <LeftMenuItemVue msg="Home" icon="home.svg" class="selected"/>
    <LeftMenuItemVue msg="Search" icon="search.svg"/>
    <LeftMenuItemVue msg="Your Library" icon="folder.svg"/>

    <div class="left-menu-gap">
        <LeftMenuItemVue msg="Create Playlist" icon="plus.svg" class="bg-light-grey hover-group"/>
        <LeftMenuItemVue msg="Liked Songs" icon="heart.svg" class="bg-purp-white hover-group"/>
    </div>

    <div class="left-seperator"></div>

    <div class="playlist">
        <LeftMenuPlaylistVue playlist="Hi Mom"/>
        <LeftMenuPlaylistVue playlist="My Cool Playlist"/>
        <LeftMenuPlaylistVue playlist="Burner Studio"/>
        <LeftMenuPlaylistVue playlist="Hot Traxs"/>
        <LeftMenuPlaylistVue playlist="Disco Down"/>
        <LeftMenuPlaylistVue playlist="Bollywood Bangers"/>
        <LeftMenuPlaylistVue playlist="Tuscan Trio"/>
        <LeftMenuPlaylistVue playlist="Wonderful Windchime"/>
        <LeftMenuPlaylistVue playlist="Dad's Drum Seshs"/>
        <LeftMenuPlaylistVue playlist="Love Ballads"/>
        <LeftMenuPlaylistVue playlist="Chill Yoga"/>
        <LeftMenuPlaylistVue playlist="Pokemon Lofi"/>
        <LeftMenuPlaylistVue playlist="Headbanging"/>
        <LeftMenuPlaylistVue playlist="2000s Heartache"/>
        <LeftMenuPlaylistVue playlist="Workout Pump"/>
        <LeftMenuPlaylistVue playlist="Xylephone Heartland Humdingers"/>
        <LeftMenuPlaylistVue playlist="Hip Hop Hula-Hoop"/>
        <LeftMenuPlaylistVue playlist="Jazzercise Jams"/>
    </div>

  </div>
</template>

<style scoped>
.left-bar{
    padding-left: 1rem;
    padding-top: .5rem;
    background-color: black;
    display: grid;
    width: inherit;
}
.dot-menu{
    width: 40px;
}

.left-menu-gap{
    margin-top: 2rem;
}

.left-seperator{
    border-top: solid rgba(255, 255, 255, 0.226);
    border-width: thin;
    width: 90%;
}

.playlist{
    overflow-y: auto;
}

.playlist::-webkit-scrollbar {
  width: .5em;
}
 
.playlist::-webkit-scrollbar-thumb {
  background-color: rgb(44, 44, 44);
}

</style>
