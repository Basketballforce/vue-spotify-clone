<script setup>

const props = defineProps({
  playlist: {
    type: String,
    required: true,
  },
  image:{
    type: String,
    required: true,
  }
});

function getimage(){
    return new URL(`../assets/${props.image}`, import.meta.url)
}
</script>

<template>
  <div class="large-card">
    <img :src="getimage()" alt="menu-item">
    <h1>{{playlist}}</h1>
    <img src="../assets/play.svg" class="play-icon" hidden>
  </div>
</template>

<style scoped>
.large-card{
    background: #aaaaaa36;
    height: fit-content;
    height: 5rem;
    margin: 1rem;
    border-radius: 3px 3px 3px 3px;
    display: inline-flex;
    align-items: center;
}

.large-card:hover{
    background: #80808091;
}

.large-card:hover > .play-icon{
  display: inline;
}


img{
    border-radius: 3px 0px 0px 3px;
    display: inline;
}

*{
    transition: 0.5s;
}

*:hover{
    cursor: pointer;
}

img{
    width: 5rem;
    height: 5rem;
}

h1{
    margin-left: 1rem;
    margin-right: 2rem;
    color: white;
    font-size: 0.9rem;
    max-width: 50ch;
    text-overflow: ellipsis;
    overflow-x: hidden;
    max-height: 60%;
    overflow-y: hidden;
}

.bg-purp-white > img:first-child{
padding: 1.8rem;
filter: blur(0.5);
background: rgb(50,22,149);
background: linear-gradient(133deg, rgba(50,22,149,1) 10%, rgba(84,53,207,1) 47%, rgba(199,235,255,1) 92%);
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
  display: none;
}

</style>
