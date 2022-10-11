<template>
    <div id="articles">
        <div class="info-container">
            <SectionTitleComponent :title="sectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. 
                Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.
            </p>
        </div>
        <div class="articles-card-container row">
            <div class="col article-card" v-for="(card, index) in cards" :key="index">
                <div class="image-container">
                    <img :src="`./assets/img/${card.imgUrl}`" :alt="card.title"/>
                </div>
                <div class="content-container">
                    <h5> {{ card.title }} </h5>
                    <p> {{ card.date }} </p>
                    <div class="line"></div>
                    <p> {{ card.content }} </p>                    
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col"></div>
            <div class="col">VIEW ALL ARTICLES</div>
            <div class="col"></div>
        </div>
    </div>
</template>

<script>
import SectionTitleComponent from './SectionTitleComponent.vue';
export default {
    name: "ArticlesComponent",
    data(){
        return {
            sectionTitle: 'Latest News',
            cards: [
                {
                    title: "Redeveloping Florida's Remote Southern Coast",
                    imgUrl: 'blog-post-134132600.jpg',
                    date: 'December 7th, 2015',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi aut, cumque totam, fugiat aliquam tempora illum quae pariatur in at iure quia et dolore esse. Aliquam illum corrupti consequatur odio.'
                },
                {
                    title: "How We Manage Large Construction Projects",
                    imgUrl: 'blog-post-92486644.jpg',
                    date: 'December 7th, 2015',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi aut, cumque totam, fugiat aliquam tempora illum quae pariatur in at iure quia et dolore esse. Aliquam illum corrupti consequatur odio.'
                },
                {
                    title: 'Future proofing a modern home',
                    imgUrl: 'blog-post-332773904.jpg',
                    date: 'December 6th, 2015',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi aut, cumque totam, fugiat aliquam tempora illum quae pariatur in at iure quia et dolore esse. Aliquam illum corrupti consequatur odio.'
                },
            ]
        }
    },
    components: { 
        SectionTitleComponent 
    }
}
</script>

<style scoped lang="scss">
  @import '@/assets/styles/pallette.scss';

    #articles{
        background-color: $pampas-color;
        padding: 10px 0;
        text-align: center;
        .info-container{
            padding-top: 0;
        }
        .articles-card-container{
            justify-content: center;
            margin: 0px 240px;
            margin-bottom: 50px;

            .article-card{
                width: calc((100% / 3) - 480px);
                margin: 0 10px;
                padding: 0;
                background-color: $white-color;
                height: 100%;
                .image-container{
                    width: 100%;
                    img{
                        height: 100%;
                        width: 100%;
                    }
                }
                .content-container{
                    padding: 15px;
                    text-align: left;
                    
                    .line{
                        border-top: 1px solid $dove-grey-color;
                        padding-bottom: 1rem;
                    }
                }
            }
        }
        .row:last-child{
            margin: 70px 150px;
            justify-content: center;


            .col{
                margin: 0 10px;

            }
            .col:first-child{
                border-top: 1px solid $white-color;
            }
            .col:last-child{
                border-bottom: 1px solid $white-color;
            }
        }
    }

</style>