<template> 
        <player></player>
</template>
<script>
import Player from '@/components/Player.vue';
export default {
    created () {
        this.$emit("switchTab","music")
    },
    components: {
        Player
    }
}
</script>
<style >

</style>
