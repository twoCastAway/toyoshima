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
            isOpen: {
                type: Boolean,
                default: false
            },
        }        
    },
    methods: {
        openSubM: function(){
            // this.$set(this.isOpen, 'default', true)
            this.isOpen = true
            console.log('open')
        },
        closeSubM: function(){
            this.isOpen = false
            console.log('close')
        }
    },
    computed: {
        a: function(){
            
        }
    }
}
</script>
<template>
    <div id="SideMenu">
        <ul>
            <li v-for="(li, id) in sideMenuList" :key="id" @mouseenter="openSubM" @mouseleave="closeSubM">
                {{ li }}
                <SubMenuList :ID="id" :v-if="isOpen" />
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
