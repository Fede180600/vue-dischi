<template>
    <section class="albums_list">
        <div class="container p-5">
            <div class="row row-cols-3 row-cols-md-6 justify-content-center">
                <AppAlbum v-for="(card, index) in albums" :key="index" :album="card"/>
            </div>
        </div>
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
    height: 80%;
}
</style>