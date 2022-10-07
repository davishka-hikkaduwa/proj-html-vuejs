<template>
    <div id="services">
        <div class="label-container">
            <h4>Do You Have A Construction Project We Can Help With?</h4>
        </div>
        <button class="sandwich-btn black-btn">GET A FREE QUOTE</button>
        <div class="info-container">
            <SectionTitleComponent :title="sectionTitle"/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, architecto. Repellendus, aut. Vitae perferendis quaerat rerum odit quibusdam voluptatibus excepturi.</p>
        </div>
        <ServicesCardComponent class="card-container"/>
        <div class="image-container">
            <div class="top-curved-space"></div>
            <div class="row card-container">
                <div class="col card" v-for="(card, index) in cards" :key="index">
                    <font-awesome-icon :icon="card.icon" class="icons"/>
                    <h5> {{ card.number }} </h5>
                    <p> {{ card.text }} </p>
                </div>
            </div>
            <div class="bottom-curved-space"></div>
        </div>
    </div>
</template>

<script>
import ServicesCardComponent from '@/components/ServicesCardComponent.vue';
import SectionTitleComponent from '@/components/SectionTitleComponent.vue';
    export default {
    name: "ServicesComponent",
    data(){
        return {
            sectionTitle: 'Specialists in Modern Construction',
            cards: [
                {
                    text: 'PLANNING APPLICATIONS', 
                    icon: 'fa-solid fa-briefcase',
                    number: 3534
                },
                {
                    text: 'COMPLETED PROJECTS', 
                    icon: 'fa-regular fa-building',
                    number: 896
                },
                {
                    text: 'TRAINED PROFESSIONALS', 
                    icon: 'fa-solid fa-users',
                    number: 172
                },
                {
                    text: 'INTERNATIONAL OFFICES', 
                    icon: 'fa-solid fa-globe',
                    number: 19
                },
            ]
        }
    },
    components: {
    ServicesCardComponent,
    SectionTitleComponent
},
}

</script>

<style scoped lang="scss">
    #services{
        text-align: center;

        .label-container{
            padding: 50px 30px;
            background-color: #f9d03f;
            color: #1e1e1e;
        }
 
        .sandwich-btn{
            display: block;
            position: absolute;
            border: 2px solid #fff;
            left: 50%;
            transform: translateY(-50%) translateX(-50%);
        }
        .sandwich-btn:hover{
            background-color: #fff;
            color: #1e1e1e;
            border: 2px solid #1e1e1e;
        }
        .card-container{
            padding: 20px 60px;
            margin-bottom: 80px;
            .row{
                flex-wrap: nowrap;
            }    
        }
        
        .image-container{
            background-image: url('@/assets/img/home-244125289.jpg');
            background-repeat:no-repeat;
            background-size: cover;
            height: 600px;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;

            .top-curved-space,
            .bottom-curved-space {
                background-color: #fff;
            }

            .card-container{
                padding: 0;
                margin: 0 200px;
                width: 100%;
                display: flex;
                justify-content: space-between;
                background-color: transparent;

                .card{
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                    background-color: transparent;
                    white-space: nowrap;
                    .icons{
                        color: #f9d03f;
                        font-size: 60px;
                        margin: 10px 0;
                    }
                    h5{
                        color: #f9d03f;
                        font-size: 50px;
                    }
                    p{
                        color: #fff;
                        font-size: 12px;
                        font-weight: bold;
                    }
                }

            }
        }
    }

</style>