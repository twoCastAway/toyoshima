<template>
    <header>
        <div id="pageConfig">
            <ul>
                <li>文字サイズ・色合い変更</li>
                <li>ふりがな表示</li>
                <li>音声読上げ</li>
            </ul>
        </div>
        <SiteMap />
        <!-- <div id="siteMap">
            <ul>
                <li>サイトマップ</li>
                <li>携帯サイト</li>
                <li>アクセス</li>
            </ul>
        </div> -->
        <div id="selectLanguage">select language</div>
        <div id="emerjency">防災・緊急重要な情報</div>
        <div id="callCenter">豊島区役所コールセンター</div>
    </header>

    <div id="mainWrapper1">
        <SideMenu />
        <!-- <div id="SideMenu">
            <ul>
                <li>防災・安全</li>
                <li>手続き・届出</li>
                <li>暮らし・地域</li>
                <li>健康・福祉</li>
                <li>子育て・教育・若者</li>
                <li>文化・観光・スポーツ</li>
                <li>まちづくり・環境・産業</li>
                <li>区政情報</li>
            </ul>
        </div> -->
        <div id="carousel">

        </div>
        <div id="attention">

        </div>

        <!-- ↓カスタム検索以降, 上から落ちるトランジションの対象 -->
        <div id="mainWrapper2">
            <div id="googleCustom">googleCustom</div>
            <div id="lifeScene">lifeScene</div>
            <div id="usefulInformation">usefulInformation</div>
            <div id="wardAdministration">wardAdministration</div>
            <div id="effort">effort</div>
            <div id="SNS">sns</div>
        </div>
    </div>

    <footer>

    </footer>
</template>

<style scoped>

</style>

<script>
import SiteMap from './components/SiteMap.vue'
import SideMenu from './components/SideMenu.vue'

export default {
    name: 'index',
    components: { 
        SiteMap ,
        SideMenu
    }
}
</script>