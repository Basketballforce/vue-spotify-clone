<script setup>

const props = defineProps({
  playlist: {
    type: String,
    required: true,
  },
});

</script>

<template>
  <div class="left-playlist">
    <p>{{playlist}}</p>
  </div>
</template>

<style scoped>
.left-playlist{
    padding-top: .5rem;
}

P{
    font-family: arial;
    max-width: 23ch;
    overflow-x: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

p:hover{
    color: white;
}

</style>
