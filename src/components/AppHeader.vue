<template>
    <header>
        <img src="../assets/img/logo.png" alt="">
    </header>
</template>

<script>
export default {
    name: "AppHeader",
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
header {
    height: 60px;
    background-color: $app-light-gray;
    display: flex;
    align-items: center;
    img {
        height: 70%;
        margin-left: 20px;
    }
}
</style>