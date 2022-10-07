<template>
<div class="services-card-container row">
    <div class="col services-card" v-for="(card, index) in cards" :key="index" 
        v-on:mouseenter="toggleCard(card)" v-on:mouseleave="toggleCard(card)">
        <div :key="card.flipped" class="inner-card">
            <div class="icon-container">
                <font-awesome-icon :icon="card.front.icon" class="icons"/>
            </div>
            <h4> {{ card.flipped ? card.back.title : card.front.title }} </h4>
            <p> {{ card.flipped ? card.back.text : card.front.text }} </p>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'ServicesCardComponent',
    props: {
        flipped: Boolean,
    },
    data(){
        return {
            // cards: [
            //     {title: 'Buildings', icon: 'fa-regular fa-building'},
            //     {title: 'Renovate', icon: 'fa-solid fa-arrows-rotate'},
            //     {title: 'Construct', icon: 'fa-solid fa-house-chimney'},
            //     {title: 'Exclusive', icon: 'fa-solid fa-truck'}
            // ]
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
                    },
                    flipped: false
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
                    },
                    flipped: false
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
                    },
                    flipped: false
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
                    },
                    flipped: false
                },
            ]
        }
    },
    methods: {
        toggleCard(card) {
            card.flipped = !card.flipped;
        },
    }

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
            border-radius: 5%;
            background-color: #f0ede6;
            align-items: center;

            .inner-card{
                // position: relative;
                background-color: #f0ede6;
                display: flex;
                justify-content: center;
                flex-direction: column;
                align-items: center;

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
    // .toggle{
    //     display: none !important;
    // }
</style>