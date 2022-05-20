<template>
    <section>
        <div v-if="loading" class="container my_load">
        <AppLoading />
        </div>
        <div v-else>
            <div class="albums_list py-4">
                <div class="container">
                    <div class="row row-cols-3 row-cols-md-6 justify-content-center">
                        <AppAlbum v-for="(card, index) in albums" :key="index" :album="card"/>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import AppAlbum from "./AppAlbum.vue";
import AppLoading from "./AppLoading.vue";
import axios from "axios";

export default {
    name: "AppAlbumsList",
    components: {
        AppAlbum,
        AppLoading,
    },
    data: function() {
        return {
            albums: [],
            loading: true,
        };
    },
    created() {
        axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((resp) => {
            this.albums = resp.data.response;
            this.loading = false;
        });
    }

}
</script>

<style lang="scss" scoped>
.my_load {
    color: white;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
</style>