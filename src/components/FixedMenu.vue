<script setup>
const props = defineProps({
    username: {
        type: String,
        required: true,
    },
});
</script>

<template>
    <div class="container-fixed-menu" id="fixed-menu-parent">
        <div id="fixed-menu">
            <img src="../assets/chevron-left.svg" title="Go Back" alt="go back" class="left-arrow" />
            <img src="../assets/chevron-right.svg" title="Go Forward" alt="go forward" class="right-arrow" />
            <span>
                <img class="user-icon" src="../assets/user.svg" />
                <p>{{ username }}</p>
                <img class="user-settings-down-arrow" src="../assets/chevron-down.svg" />
            </span>
        </div>
    </div>
</template>

<style scoped>
#fixed-menu {
    position: fixed;
    padding-top: 1rem;
    padding-bottom: 1rem;
    padding-left: 1rem;
    width: inherit;
    max-width: inherit;
    background: rgb(4, 9, 61);
}

img {
    background: rgba(0, 0, 0, 0.803);
    border-radius: 50px;
    margin-right: 0.5rem;
    margin-left: 0.5rem;
    padding: 0.25rem;
    cursor: pointer;
}

.left-arrow {
    padding-right: 0.3rem;
}

.right-arrow {
    padding-left: 0.3rem;
}

.container-fixed-menu {
    width: 100%;
    height: 4rem;
    z-index: 1;
}

span {
    float: right;
    margin-right: 2rem;
    background: black;
    padding-left: 1rem;
    padding-top: 0.25rem;
    padding-bottom: 0.25rem;
    border-radius: 25px;
    padding-top: 3px;
    padding-bottom: 3px;
}

span:hover {
    background: rgb(39, 39, 39);
}

.user-settings-down-arrow {
    vertical-align: middle;
    margin-top: -0.2rem;
    background: none;
    margin-right: 0.1rem;
    margin-left: 0.3rem;
}

.user-icon {
    padding: 0.15rem;
    margin: 0;
    vertical-align: middle;
    margin-left: -0.9rem;
    margin-right: 0.6rem;
    background: grey;
}

p {
    display: inline;
    color: white;
}

.left-arrow:hover,
.right-arrow:hover {
    background: rgba(0, 0, 0, 0.503);
}
</style>

<script scoped>
window.addEventListener("load", function () {
    const parentElement = document.getElementById("fixed-menu-parent");
    const fixedElement = document.getElementById("fixed-menu");

    window.addEventListener("resize", changeFixedElementWidth);

    function changeFixedElementWidth() {
        const parentElementWidth = parentElement.getBoundingClientRect().width;
        fixedElement.style.width = parentElementWidth + "px";
    }

    changeFixedElementWidth();
});
</script>
