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
    <div class="friend-header">
        <p class="friend-activity">Friend Activity</p>
        <div>
            <img class="icon-spacer" src="../assets/user-plus.svg" alt="">
            <img class="icon-spacer" id="close-friend" src="../assets/x.svg" alt="">
        </div>
    </div>

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
.friend-activity {
    margin-top: 2rem;
    margin-left: 1rem;
    font-size: 1rem;
}

img {
    vertical-align: middle;
}

.friend-header {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;

}

.icon-spacer {
    margin-right: 1rem;
    filter: brightness(0.5);
    cursor: pointer;
}

.icon-spacer:hover {
    filter: brightness(1);
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

<script>
window.addEventListener('load', function () {
const mainGrid = document.getElementById('main-grid');
const closefriend = document.getElementById('close-friend');

closefriend.addEventListener('click', closeFriendPane);

function closeFriendPane() {
mainGrid.style.gridTemplateColumns = '1fr 4fr';
}

})
</script>