<template>
<div class="services-card-container">
    <div class="col-3 services-card" v-for="(item, index) in items" :key="index">
        <div class="icon-container">
            <font-awesome-icon :icon="item.icon" class="icons"/>
        </div>
        <h4> {{ item.title }} </h4>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Recusandae, fugit. Sint corrupti tenetur vitae.
        </p>
    </div>
</div>
</template>

<script>
export default {
    name: 'ServicesCardComponent',
    data(){
        return {
            items: [
                {title: 'Buildings', icon: 'fa-regular fa-building'},
                {title: 'Renovate', icon: 'fa-solid fa-arrows-rotate'},
                {title: 'Construct', icon: 'fa-solid fa-house-chimney'},
                {title: 'Exclusive', icon: 'fa-solid fa-truck'}
            ]
        }
    },

}

</script>

<style scoped lang="scss">
    .services-card-container{
        display: flex;
        flex-direction: row;
        

        .services-card{
            display: flex;
            flex-direction: column;
            margin: 0 5px;
            padding: 10px;
            border-radius: 5%;
            background-color: #f0ede6;
            align-items: center;

            .icon-container{
                display: flex;
                justify-content: center;
                border: 1px solid #6b6868;
                border-radius: 50%;
                width:min-content;
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