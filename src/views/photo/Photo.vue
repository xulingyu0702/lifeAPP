<template>
    <div>
       <h1>照片</h1> 
    </div>
</template>
<script>
export default {
    created(){
        this.$emit("switchTab","photo")
    }
}
</script>
<style lang="sass" scoped>

</style>
