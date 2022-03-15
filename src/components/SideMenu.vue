<script>
import SubMenuList from './child/SubMenuList.vue'
export default {
    name: 'SideMenu',
    components: {
        SubMenuList
    },
    props: {
        subMenuID: {
            type: Number,
            default: null,
            validator: function(value){
                if(value < 8){
                    return
                } else{
                    console.log('error')
                }
            },
            requried: true
        },
        // isOpen: {
        //     type: Boolean,
        //     default: false
        // }
    },
    data(){
        return{
            sideMenuList: [
                    '防災・安全',
                    '手続き・届出',
                    '暮らし・地域',
                    '健康・福祉',
                    '子育て・教育・若者',
                    '文化・観光・スポーツ',
                    'まちづくり・環境・産業',
                    '区政情報',
            ],
        }        
    },
}
</script>
<template>
    <div id="SideMenu">
        <ul>
            <li v-for="(li, id) in sideMenuList" :key="id" v-on:mouseover="openSubM, isOpen" >{{ li }}</li>
        </ul>
    </div>
    <SubMenuList />
</template>
<style scoped>
#SideMenu > ul > li {
    list-style-type: none;
}
#SideMenu {
    display: flex;
}
</style>
