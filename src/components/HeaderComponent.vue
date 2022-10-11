<template>
    <header>
        <div class="row">
            <div class="col-6">
                <div class="img-container">
                    <img src="../assets/img/construction_logo.png" alt="logo">
                </div>
            </div>
            <div class="col-4 list-container">
                <ul>
                    <li v-for="item in items" :key="item">
                        {{ item }}
                    </li>                
                </ul>
            </div>
            <div class="col-2">
                <div class="button-container">
                    <button class="gold-btn">GET A QUOTE</button>    <!-- BUTTON -->
                </div>
            </div> 
        </div>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data() {
            return {
                items: ['HOME', 'ABOUT', 'SERVICES', 'WORK', 'ARTICLES']
            }
        }
    }

</script>

<style scoped lang="scss">
@import '@/assets/styles/pallette.scss';

    header{
        margin: 0;
        height: 100px;
        .row{
            height: 100%;
        }
        .img-container{
            height: 80%;
            width: 80%;
            padding-left: 50px;
            padding-top: 20px;
            img{
                max-height: 100%;
                max-width: 100%;
            }
        }

        ul{
            list-style-type: none;
            justify-content: space-between;
            li{
                color: $dove-grey-color;
            }
            li:hover{
                color: $bright-sun-color;
            }     
        }
        .button-container{
            justify-content: center;      
        }
        ul, .button-container{
            display: flex;
            align-items: center;
            height: 100%;
        }
               
    }
    
    
   
</style>