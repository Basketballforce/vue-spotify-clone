<script setup>

const props = defineProps({
  category: {
    type: String,
    required: true,
  },
});

function getimage(){
    return new URL(`../assets/${props.image}`, import.meta.url)
}
</script>

<template>
  <div class="category-title">
    <h1>{{category}}</h1>
    <p>SEE ALL</p>
  </div>
</template>

<style scoped>
h1{
    margin-left: 1rem;
    margin-right: 2rem;
    margin-top: .75rem;
    margin-bottom: 0.25rem;
    color: white;
    font-size: 1.25rem;
    max-width: 50ch;
    text-overflow: ellipsis;
    overflow-x: hidden;
    max-height: 60%;
    overflow-y: hidden;
}

p{
    margin-left: 1rem;
    margin-right: 2rem;
    font-size: 0.7rem;
    max-width: 30ch;
    text-overflow: ellipsis;
    overflow: hidden;
    max-height: 2rem;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}

p:hover, h1:hover{
    text-decoration: underline;
    cursor: pointer;
}

.category-title{
    display: flex;
    flex-wrap: nowrap;
    justify-content: space-between;
    margin-left: 1rem;
    align-items: baseline;
}

</style>
