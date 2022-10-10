<template>
    <div class="card-back-icons">
        <div class="col icon-container">
            <font-awesome-icon icon="fa-solid fa-link" class="icons"/>
        </div>
        <div class="col icon-container">
            <font-awesome-icon icon="fa-solid fa-magnifying-glass" class="icons"/>
        </div>                           
    </div>
</template>

<script>
    export default {
        name: 'CardBackIconsComponent',
    }
</script>

<style scoped lang="scss">

    .icon-container{
        border-radius: 50%;
        padding: 22px;
        height: 35px;
        width: 35px;
        margin: 5px 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: #fff;
        cursor: pointer;

        .icons{
            color: #f9d03f;
        }
    }
</style>