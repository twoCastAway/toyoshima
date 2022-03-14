<template>
    <div id="SideMenu">
        <ul>
            <li v-for="(li, id) in sideMenuList" :key="id" @click="Click">{{ li }}</li>
            <!-- <li>手続き・届出</li>
            <li>暮らし・地域</li>
            <li>健康・福祉</li>
            <li>子育て・教育・若者</li>
            <li>文化・観光・スポーツ</li>
            <li>まちづくり・環境・産業</li>
            <li>区政情報</li> -->
        </ul>
    </div>
</template>
<style scoped>
#SideMenu > ul > li {
    list-style-type: none;
}
</style>
<script>
export default {
    name: 'SideMenu',
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
            subMenuList: [
                {},
                {},
                {},
                {},
                {},
                {},
                {},
                {}
            ]
        }        
    },
    methods: {
        // Click: function(){
        //     //click→hover
        //     //サブメニューリストを表示
        //     //debounce
        // }
    }
}
</script>
