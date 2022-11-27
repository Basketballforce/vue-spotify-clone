<script setup>

const props = defineProps({
  playlist: {
    type: String,
    required: true,
  },
  image:{
    type: String,
    required: true,
  },
  artists_or_description:{
    type: String,
    required: true,
  },
});

function getimage(){
    return new URL(`../assets/${props.image}`, import.meta.url)
}
</script>

<template>
  <div class="square-card">

    <div>
        <img :src="getimage()" alt="menu-item">
        <img src="../assets/play.svg" class="play-icon" hidden>
        <h1>{{playlist}}</h1>
        <p>{{artists_or_description}}</p>
    </div>
  </div>
</template>

<style scoped>
.square-card{
    background: #171717;
    height: fit-content;
    height: 17.5rem;
    padding-left: 1rem;
    padding-right: 1rem;
    padding-bottom: 2rem;
    padding-top: 1rem;
    margin-top: 1rem;
    margin-right: 1.25rem;
    width: 12rem;
    border-radius: 6px;
}

.square-card:hover{
    background: #80808033;
}

.square-card:hover > div > .play-icon{
  display: inline;
  position: absolute;
  /* Appear animation/ slide up */
}


img{
    border-radius: 3px 3px 3px 3px;
    height: 10rem;
    width: 10rem;
    display: block;
    margin: auto;
    object-fit: cover;
}

*{
    transition: 0.5s;
}

*:hover{
    cursor: pointer;
}

h1{
    margin-right: 1rem;
    margin-top: .75rem;
    color: white;
    font-size: 0.80rem;
    max-width: 50ch;
    text-overflow: ellipsis;
    overflow-x: hidden;
    max-height: 60%;
    overflow-y: hidden;
    white-space: nowrap;
}

.play-icon{
  background: rgb(35, 192, 35);
  border-radius: 50px;
  width: 3rem;
  height: 3rem;
  margin-left: auto;
  margin-right: 1rem;
  padding-left: 0.8rem;
  padding-right: 0.6rem;
  padding-top: 0.65rem;
  padding-bottom: 0.65rem;
  display: none;
  transition: .15s;
  top: 6.5rem;
  left: 6.5rem;
}

.play-icon:hover{
  transform: scale(1.1);
  transition: 0.15s;
  background: rgb(38, 201, 38);
}

.play-icon:active{
  background: rgb(25, 141, 25);
}

p{
    margin-right: 1rem;
    margin-top: 0.25rem;
    font-size: 0.74rem;
    max-width: 30ch;
    text-overflow: ellipsis;
    overflow: hidden;
    max-height: 2rem;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    font-family: arial;
    font-weight: 500;
}

</style>
