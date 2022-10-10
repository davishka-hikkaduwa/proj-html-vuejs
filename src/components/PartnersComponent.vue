<template>
    <div id="trusted-partners">
        <div class="info-container">
            <SectionTitleComponent :title="sectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.</p>

        </div>
    </div>
</template>

<script>
import SectionTitleComponent from '@/components/SectionTitleComponent.vue';
export default {
    name: "PartnersComponent",
    data(){
        return {
            sectionTitle: 'Trusted Partners'
        }
    },
    components: { SectionTitleComponent }

}

</script>

<style scoped lang="scss">
    #trusted-partners{
        text-align: center;
    }
</style>