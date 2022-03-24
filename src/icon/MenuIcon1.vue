<template>
    <!-- <a href="" v-on:click="Click"></a> -->
    <div :id="iconID">
        <img :src="src" :alt="alt">
        <p>{{ iconName }}</p>
    </div>
</template>

<style scoped>

</style>

<script>
export default {
    name: 'MenuIcon1',
    data() {
        return {
            iconID: '',
            iconName: '',
            href: '',
            src: '',
            alt: '',
        }
    },
    methods: {
        
    },
}
</script>
