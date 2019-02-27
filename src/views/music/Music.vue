<template> 
        <player :musicList="musicList"></player>
</template>
<script>
import Player from '@/components/Player.vue';
import axios from 'axios'
export default {
    data(){
       return{
            musicList:[],
       }
    },
    created () {
        this.$emit("switchTab","music");
        axios.get('/data/musicdata.json').then(res=>{
            console.log(res)
            this.musicList=res.data.musicData
        })
    },
    components: {
        Player
    }
}
</script>
<style >

</style>
