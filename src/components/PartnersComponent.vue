<template>
    <div id="trusted-partners">
        <div class="info-container">
            <SectionTitleComponent :title="infoSectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.</p>          
        </div>
        <div class="card-container row">
            <div class="card col" v-for="(card, index) in cards" :key="index">
                <img :src="`./assets/img/${card.url}`" :alt="index"/>
            </div>
        </div>
        <div class="jumbotron row">
            <div class="col-8 container">
                <SectionTitleComponent :title="jumbotronSectionTitle"/>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi ipsam, assumenda perferendis fugit.</p>
            </div>
            <div class="col-4 container">
                <button class="gold-btn">GET A FREE QUOTE</button>
                <p>Only takes a few seconds!</p>
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
            infoSectionTitle: 'Trusted Partners',
            jumbotronSectionTitle: 'Building Inspiring Spaces',
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
        .jumbotron{
            padding: 20px 150px;
            margin-top: 70px;
            background-image: url('@/assets/img/about-call-to-action-57862405.jpg');
            background-repeat:no-repeat;
            background-size: cover;
            background-position-y: 80%;   
            color: #fff;
            height: 300px;
            .container{
                border: 1px solid #fff;
                display: flex;
                flex-direction: column;
                justify-content: center;
            }   
            .container.col-8{
                text-align: left;               
                align-items: flex-start;
                padding: 0 20px;

            }
            .container.col-4{
                padding: 0 40px;
                button{
                    margin: 10px 0;
                }
                p{
                    font-size: 0.8rem;
                    font-weight: bold;
                }
            }
        }
    }
</style>