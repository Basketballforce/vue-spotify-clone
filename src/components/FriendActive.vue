<script setup>

const props = defineProps({
    username: {
        type: String,
        required: true,
    },
    profilepic: {
        type: String,
        required: true,
    },
    song: {
        type: String,
        required: true,
    },
    artist: {
        type: String,
        required: true,
    },
    album: {
        type: String,
        required: true,
    },
});

function getimage() {
    return new URL(`../assets/${props.profilepic}`, import.meta.url)
}

</script>

<template>
    <div class="friend">
        <div>
            <img :src="getimage()" alt="" class="friend-profile-pic">
            <h3>{{username}}</h3>
            <p class="friend-details">{{song}} •{{artist}} ⊚{{album}}</p>
        </div>
        <p class="last-active-friend"> 2d</p>
    </div>
</template>

<style scoped>

img {
    vertical-align: middle;
}

.friend-profile-pic {
    height: 3rem;
    width: 3rem;
    border-radius: 50px;
    object-fit: cover;
    margin-right: 1rem;
}

.friend {
    margin-top: 1rem;
    margin-left: 1rem;
    margin-bottom: 1rem;
    display: flex;
    justify-content: space-between;
}

.last-active-friend {
    line-height: 26px;
    margin-right: 2rem;
}

h3{
    display: inline;
    vertical-align: top;
}

.friend-details{
    margin-left: 4rem;
    margin-top: -1.5rem;
    font-family: arial;
    font-size: .75rem;
}

</style>