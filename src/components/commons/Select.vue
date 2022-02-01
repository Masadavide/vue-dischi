<template>
    <select name="genre" @change="$emit('genre', selected)" v-model="selected" class="input">
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
    </select>
    
</template>

<script>
export default {
    name: 'Select',
    data() {
        return {
            selected: ""
        }
    }
}

</script>

<style lang='scss' scoped>
    .input{
        margin: 0 auto;
    }
</style>