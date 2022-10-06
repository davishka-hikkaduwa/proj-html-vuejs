<template>
    <main>
        <HomeComponent/>
        <ServicesComponent/>
        <WorkComponent/>
        <AboutComponent/>
    </main>
</template>

<script>
import HomeComponent from '@/components/HomeComponent.vue';
import ServicesComponent from '@/components/ServicesComponent.vue';
import WorkComponent from '@/components/WorkComponent.vue';
import AboutComponent from '@/components/AboutComponent.vue';
export default {
    name: "MainComponent",
    components: {
    HomeComponent,
    ServicesComponent,
    WorkComponent,
    AboutComponent
}
}
</script>

<style scoped lang="scss">

</style>