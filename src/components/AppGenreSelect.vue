<template>
    <div>
        <select class="form-select container mt-4 " aria-label="Default select example" v-model="selectedGenre" @change="$emit('searchGenre', selectedGenre)">
            <option value="" selected disabled>Seleziona il genere</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
            <option value="Pop">Pop</option>
            <option value="Rock">Rock</option>

        </select>
    </div>
</template>
<script>
export default {
    name: "AppGenreSelect",
    data: function() {
        return {
            selectedGenre: "",
        };
    },
    created: function() {
        this.selectedGenre = this.selectedGenre.value;
    }
}
</script>
<style lang="scss" scoped>
</style>