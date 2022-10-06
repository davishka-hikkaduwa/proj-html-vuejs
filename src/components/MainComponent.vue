<template>
    <main>
        <HomeComponent/>
        <ServicesComponent/>
    </main>
</template>

<script>
import HomeComponent from '@/components/HomeComponent.vue';
import ServicesComponent from '@/components/ServicesComponent.vue';
export default {
    name: "MainComponent",
    components: {
        HomeComponent,
        ServicesComponent
    }
}
</script>

<style scoped lang="scss">

</style>