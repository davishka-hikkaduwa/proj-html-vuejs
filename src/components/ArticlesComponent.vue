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
                    <img src="@/assets/img/blog-post-134132600.jpg" alt="img-1">
                </div>
                <div class="content-container">
                    <h5> {{ card.title }} </h5>
                    <p> {{ card.date }} </p>
                    <div>


                    </div>
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
                    title: 'Redeveloping',
                    imgUrl: '#',
                    date: 'December 7th, 2015',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi aut, cumque totam, fugiat aliquam tempora illum quae pariatur in at iure quia et dolore esse. Aliquam illum corrupti consequatur odio.'
                },
                {
                    title: 'How We Manage',
                    imgUrl: '#',
                    date: 'December 7th, 2015',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi aut, cumque totam, fugiat aliquam tempora illum quae pariatur in at iure quia et dolore esse. Aliquam illum corrupti consequatur odio.'
                },
                {
                    title: 'Future Proofing',
                    imgUrl: '#',
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
    #articles{
        background-color: #f0ede6;
        padding: 10px 0;
        text-align: center;
        .info-container{
            padding-top: 0;
        }
        .articles-card-container{
            justify-content: center;
            height: 400px;
            margin: 0px 150px;
            margin-bottom: 50px;

            .article-card{
                border: 1px solid black;
                margin: 0 10px;
                padding: 0;
                .image-container{
                    height: 40%;
                    width: 100%;
                    img{
                        height: 100%;
                        width: 100%;
                    }
                }
                .content-container{
                    padding: 15px 10px;
                    text-align: left;
                }
            }
        }
        .row:last-child{
            margin: 50px 150px;
            justify-content: center;


            .col{
                margin: 0 10px;

            }
            .col:first-child{
                border-top: 1px solid #fff;
            }
            .col:last-child{
                border-bottom: 1px solid #fff;
            }
        }
    }

</style>