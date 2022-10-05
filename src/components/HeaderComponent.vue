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
                    <button>GET A QUOTE</button>    <!-- BUTTON -->
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
    
    header{
        margin: 0;
        height: 100px;
        border-bottom: 1px solid black;
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
                color: #6b6868;
            }
            li:hover{
                color: #fed23f;
            }     
        }
        .button-container{
            justify-content: center;
            button{
                background-color: #f9d03f;
                color: #6b6868;
                border: none;
                padding: 10px 20px;
            }      
        }
        ul, .button-container{
            display: flex;
            align-items: center;
            height: 100%;
        }       
    }
    
    
   
</style>