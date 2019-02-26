<template>
    <div>
       <h1>书</h1> 
    </div>
</template>
<script>
export default {
    created(){
        this.$emit("switchTab","book");
    }
}
</script>
<style lang="sass" scoped>

</style>
