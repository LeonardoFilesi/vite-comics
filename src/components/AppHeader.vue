<script>

export default {
  components: {
    name: "AppHeader",
  },
  data() {
    return {
        headerNav: [
                {text: "CHARACTERS"}, { text: `COMICS`}, {text: `MOVIES`}, {text: `TV`}, {text: `GAMES`}, {text: `COLLECTIBLES`}, {text: `VIDEOS`}, {text: `FANS`}, {text: `NEWS`}, {text: `SHOP`},
        ]
    }
    }
}
</script>

<template>
        <div class="ms_container flex">
            <div class="logoContainer"><img src="../assets/dc-logo.png" alt=""></div>
            <ul class="flex">
                <li v-for="item in headerNav">
                    {{ item.text }}
                </li>
            </ul>
        </div>
</template>

<style lang="scss" scoped>
.ms_container {
  width: 100%;
  padding: 10px 10%;
  justify-content: space-between;
}

/* .logoContainer {

} */
.flex {
  display: flex;
}

ul {
    list-style-type: none;
    align-items: center;
}

li {
    margin-left: 20px;
}
</style>