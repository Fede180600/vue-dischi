<template>
    <div class="album_card">
        <div class="card_img">
            <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
        </div>
        <div class="album_description">
            <h3>Nome Album</h3>
            <p>Autore</p>
            <p>year</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "AppAlbum",
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
.album_card {
    width: calc(95% / 5 - 40px);
    padding: 20px;
    margin: 10px 20px;
    background-color: $app-light-gray;
    min-height: 200px;
    .card_img {
        width: 100%;
        height: 0;
        padding-bottom: 100%;
        object-fit: cover;
        margin-bottom: 15px;
    }
    .album_description {
        text-align: center;
        h3 {
            color: white;
            text-transform: uppercase;
            font-size: 18px;
            margin-bottom: 10px;
        }
        p {
            font-size: 14px;
            color: $app-card-text;
        }
    }
}
</style>