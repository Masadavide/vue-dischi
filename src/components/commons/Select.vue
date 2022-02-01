<template>
    <select name="genre" @change="passaSelect">
        <option value="null">Seleziona un genere</option>
        <option value="rock">Rock</option>
        <option value="pop">Pop</option>
        <option value="jezz">Jezz</option>
        <option value="metal">Metal</option>
    </select>
    
</template>

<script>
export default {
    name: 'Select',
    data() {
        return {
            t: this.genre.value,
        }
    },
    methods: {
        passaSelect: function(e){
            this.$emit('genre', e.target.value)
            console.log(e.target.value)

        }
    }
}

</script>

<style lang='scss' scoped>
    

</style>