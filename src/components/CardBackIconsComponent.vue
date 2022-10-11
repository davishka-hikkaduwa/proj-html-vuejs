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
  @import '@/assets/styles/pallette.scss';

    .icon-container{
        border-radius: 50%;
        padding: 22px;
        height: 35px;
        width: 35px;
        margin: 5px 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: $white-color;
        cursor: pointer;

        .icons{
            color: $bright-sun-color;
        }
    }
</style>