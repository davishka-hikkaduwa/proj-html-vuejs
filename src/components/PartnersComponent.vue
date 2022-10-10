<template>
    <div id="trusted-partners">
        <div class="info-container">
            <SectionTitleComponent :title="sectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.</p>          
        </div>
        <div class="card-container row">
            <div class="card col" v-for="(card, index) in cards" :key="index">
                <!-- <img :src="card.url" :alt="card.number"> -->
                <img :src="`./assets/img/${card.url}`" :alt="index"/>
            </div>
        </div>
    </div>
</template>

<script>
import SectionTitleComponent from '@/components/SectionTitleComponent.vue';
export default {
    name: 'PartnersComponent',
    data(){
        return {
            sectionTitle: 'Trusted Partners',
            cards: [
                {
                    url: 'home-logo11-219096700-320x202.png'
                },
                {
                    url: 'home-logo10-219096700-320x202.png'
                },
                {
                    url: 'home-logo2-219096700-320x202.png'
                },
                {
                    url: 'home-logo1-219096700-320x202.png'
                },
                {
                    url: 'home-logo9-219096700-320x202.png'
                },
            ],
        }
    },
    components: { SectionTitleComponent }

}

</script>

<style scoped lang="scss">
    #trusted-partners{
        text-align: center;
        .card-container{
            margin: 10px 150px;
            .card{
                // border: 1px solid black;
                margin: 0 10px;
            }
        }
    }
</style>