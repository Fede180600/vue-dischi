<template>
    <section class="albums_list">
        <AppAlbum v-for="(card, index) in albums" :key="index" :album="card"/>
    </section>
</template>

<script>
import AppAlbum from "./AppAlbum.vue";
import axios from "axios";

export default {
    name: "AppAlbumsList",
    components: {
        AppAlbum,
    },
    data: function() {
        return {
            albums: [],
        };
    },
    created() {
        axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((resp) => {
            this.albums = resp.data.response;
        });
    }

}
</script>

<style lang="scss" scoped>
.albums_list {
    width: 60%;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
</style>