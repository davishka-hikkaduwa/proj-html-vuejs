<template>
    <div id="work">
        <div class="info-container">
            <SectionTitleComponent :title="sectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto.
                 Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.
            </p>
        </div>
        <div class="row card-container">
            <div class="col-4 card" v-for="(card, index) in cards" :key="index">
                <div class="inner-card">
                    <div class="card-face face-front">
                        <img :src="`./assets/img/${card.front.url}.jpg`" :alt="card.front.alt"/>
                    </div>
                    <div class="card-face face-back">
                        <CardBackIconsComponent class="row"/>
                        <div class="row">
                            <h5> {{ card.back.name }} </h5>
                            <p> {{ card.back.type }} </p>
                        </div>
                    </div>
                </div>
            </div>
            <!--
                <img src="@/assets/img/project2-featured-15013609-800x800.jpg" alt="project-2-800x800">
                <img src="@/assets/img/project1-featured-294276386-800x800.jpg" alt="project-1-800x800">
                <img src="@/assets/img/project3-featured-189023420-800x800.jpg" alt="project-3-800x800">
            -->
        </div>
        <div class="row link-container">
            <div class="col-4"></div>
            <div class="col-4">
                <a href="#">VIEW ALL PROJECTS</a>
            </div>
            <div class="col-4"></div>
        </div>
    </div>
</template>

<script>
import SectionTitleComponent from '@/components/SectionTitleComponent.vue';
import CardBackIconsComponent from '@/components/CardBackIconsComponent.vue';

export default {
    name: 'WorkComponent',
    data(){
        return {
            sectionTitle: 'Explore Recent Work',
            cards: [
                {
                    front: {
                        url: 'project2-featured-15013609-800x800',
                        alt: 'project-2-800x800'
                    },
                    back: {
                        name: 'Florida Health Facility',
                        type: 'Commercial' 
                    }
                },
                {
                    front: {
                        url: 'project1-featured-294276386-800x800',
                        alt: 'project-1-800x800'
                    },
                    back: {
                        name: 'Florida Health Facility',
                        type: 'Commercial' 
                    }
                },
                {
                    front: {
                        url: 'project3-featured-189023420-800x800',
                        alt: 'project-3-800x800'
                    },
                    back: {
                        name: 'Florida Health Facility',
                        type: 'Commercial' 
                    }
                }
            ]
        }
    },
    components: {
    SectionTitleComponent,
    CardBackIconsComponent
}
}

</script>

<style scoped lang="scss">
  @import '@/assets/styles/pallette.scss';

    #work{
        padding: 10px 0;
        text-align: center;

        .info-container{
            padding-top: 0;
        }
        
        .card-container{
            justify-content: center;
            
            .card{
                padding: 0;
                width: 250px;
                height: 250px;
                margin: 0 10px;
                
                .inner-card{
                    position: relative;
                    height: 100%;
                    width: 100%;

                    .card-face{
                        position: absolute;
                        height: 100%;
                        width: 100%;
                        backface-visibility: hidden;

                    }
                    .face-front{
                        background-color: $pampas-color;
                        display: flex;
                        justify-content: center;
                        flex-direction: column;
                        align-items: center;
                        z-index: 100;
                        img{
                            height: 100%;
                            width: 100%;
                        }
                    }

                    .face-back{
                        display: flex;
                        flex-direction: column;
                        align-items: center;
                        justify-content: center;
                        background-color: $bright-sun-color;
                        color: $white-color;

                        h5{
                            padding-top: 10px;
                        }
                        
                    }
                }
                .inner-card:hover{
                    .face-front{
                        z-index: -200;
                    }
                }

                
            }
        }
        .link-container{
            padding: 60px 200px;
            .col-4{
                a{
                    text-decoration: none;
                    font-size: 0.8rem;
                }
            }
            .col-4:first-child{
                border-top: 1px solid $pampas-color;
            }
            .col-4:last-child{
                border-bottom: 1px solid $pampas-color;
            }
            
        }
    }
</style>