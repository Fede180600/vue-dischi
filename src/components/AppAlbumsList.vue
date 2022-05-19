<template>
    <section class="albums_list">
        <AppAlbum />
        <AppAlbum />
        <AppAlbum />
        <AppAlbum />
        <AppAlbum />
        <AppAlbum />
        <AppAlbum />
        <AppAlbum />
        <AppAlbum />
        <AppAlbum />
    </section>
</template>

<script>
import AppAlbum from "./AppAlbum.vue";
export default {
    name: "AppAlbumsList",
    components: {
        AppAlbum,
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