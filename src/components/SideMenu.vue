<script>
import SubMenuList from './child/SubMenuList.vue'
export default {
    name: 'SideMenu',
    components: {
        SubMenuList
    },
    props: {
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
    methods: {
        openSubM: function(){
            
            console.log('open')
        },
        closeSubM: function(){
            console.log('close')
        }
    }
}
</script>
<template>
    <div id="SideMenu">
        <ul>
            <li v-for="(li, id) in sideMenuList" :key="id" v-on:mouseenter="openSubM" v-on:mouseleave="closeSubM">
                {{ li }}
                <SubMenuList :id="id" />
            </li>
        </ul>
    </div>
</template>
<style scoped>
#SideMenu > ul > li, #SunMenuList > ul > li {
    list-style-type: none;
}
#SideMenu {
    display: flex;
}
</style>
