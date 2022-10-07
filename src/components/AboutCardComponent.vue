<template>
    <div class="about-card-container row">
        <div class="col about-card" v-for="(card, index) in cards" :key="index">
            <div class="icon-container">
                <font-awesome-icon :icon="card.icon" class="icons"/>
            </div>
            <h6 class="custom-underline-black"> {{ card.title }} </h6>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Recusandae, fugit. Sint corrupti tenetur vitae.
            </p>
        </div>

    </div>
</template>

<script>
export default {
    name: 'AboutCardComponent',
    data(){
        return {
            cards: [
                {title: 'Great Services', icon: 'fa-solid fa-house-chimney'},
                {title: 'Highest Standards', icon: 'fa-solid fa-gear'},
                {title: 'Professional Team', icon: 'fa-solid fa-users'},
                {title: 'Creative Solutions', icon: 'fa-solid fa-lightbulb'}
            ]
        }
    }
}

</script>

<style scoped lang="scss">
    .about-card-container{

        .about-card{
            display: flex;
            flex-direction: column;
            margin: 0 5px;
            padding: 10px;
            align-items: center;

            .icon-container{
                display: flex;
                justify-content: center;
                align-items: center;
                border-radius: 50%;
                width: 100px;
                height: 100px;
                padding: 20px;
                margin: 10px 0px;

                .icons{
                    font-size: 3rem;
                    color: #fff;
                
                }
            }
            p{
                padding-top: 20px;
            }
            .custom-underline-black {
                padding-bottom: 15px;
                position: relative;
            }

            .custom-underline-black::before {
                content: '';
                position: absolute;
                bottom: 0;
                left: 40%;
                width: 25px;
                height: 2px;
                background-color: #31312f;
            }
        }

        .about-card:nth-of-type(1){
            .icon-container{
                background-color: #4da4a5;
            }
        }
        .about-card:nth-of-type(2){
            .icon-container{
                background-color: #4f6da5;
            }
        }
        .about-card:nth-of-type(3){
            .icon-container{
                background-color: #f5722b;
            }
        }
        .about-card:nth-of-type(4){
            .icon-container{
                background-color: #a7cf47;
            }
        }
    }
    
    
    
</style>