<template>
<div class="services-card-container row">
    <div class="col services-card" v-for="(card, index) in cards" :key="index">
        <div class="inner-card">
            <div class="card-face face-front">
                <div class="icon-container">
                    <font-awesome-icon :icon="card.front.icon" class="icons"/>
                </div>
                <h4> {{ card.front.title }} </h4>
                <p> {{ card.front.text }} </p>
            </div>
            <div class="card-face face-back">
                <h5> {{ card.back.title }} </h5>
                <p> {{ card.back.text }} </p>
                <button class="yellow-btn">GET A QUOTE</button>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'ServicesCardComponent',
    data(){
        return {
            cards: [
                {
                    front: {
                        title: 'Buildings', 
                        icon: 'fa-regular fa-building',
                        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, fugit. Sint corrupti tenetur vitae.' 
                    },
                    back: {
                        title: 'ARTFULLY CRAFTED',
                        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, fugit. Sint corrupti tenetur vitae.' 
                    }
                },
                {
                    front: {
                        title: 'Renovate',
                        icon: 'fa-solid fa-arrows-rotate',
                        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, fugit. Sint corrupti tenetur vitae.' 
                    },
                    back: {
                        title: 'ARTFULLY CRAFTED',
                        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, fugit. Sint corrupti tenetur vitae.' 
                    }
                },
                {
                    front: {
                        title: 'Construct',
                        icon: 'fa-solid fa-house-chimney',
                        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, fugit. Sint corrupti tenetur vitae.' 
                    },
                    back: {
                        title: 'ARTFULLY CRAFTED',
                        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, fugit. Sint corrupti tenetur vitae.' 
                    }
                },
                {
                    front: {
                        title: 'Exclusive',
                        icon: 'fa-solid fa-truck',
                        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, fugit. Sint corrupti tenetur vitae.' 
                    },
                    back: {
                        title: 'ARTFULLY CRAFTED',
                        text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae, fugit. Sint corrupti tenetur vitae.' 
                    }
                },
            ]
        }
    },


}

</script>

<style scoped lang="scss">
    .services-card-container{
        flex-wrap: nowrap;

        .services-card{
            display: flex;
            flex-direction: column;
            margin: 0 5px;
            padding: 10px;
            align-items: center;
            width: 200px;
            height: 260px;

            .inner-card{
                position: relative;
                width: 100%;
                height: 100%;
            }

            .card-face{
                position: absolute;
                padding: 20px;
                width: 100%;
                height: 100%;
                text-align: center;
                backface-visibility: hidden;
                border-radius: 5%;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                p{
                    font-size: 0.8rem;
                }

            }

            .face-front{
                background-color: #f0ede6;
                display: flex;
                justify-content: center;
                flex-direction: column;
                align-items: center;
                z-index: 100;
            }
            .inner-card:hover{
                .face-front{
                    z-index: -200;;
                }
            }

            .face-back{
                background-color: #f9d03f;
                color: #6b6868;
                .yellow-btn{
                    background-color: #ffe07b;
                    color: #6b6868;
                    cursor: pointer;

                }
            }

            

            .icon-container{
                display: flex;
                justify-content: center;
                align-items: center;
                height: 50px;
                width: 50px;
                border: 1px solid #6b6868;
                border-radius: 50%;
                padding: 15px;
                margin: 10px 0px;

                .icons{
                    font-size: 1.5rem;
                    color: #6b6868;
                }
                
            }
            
        }   
    }

</style>