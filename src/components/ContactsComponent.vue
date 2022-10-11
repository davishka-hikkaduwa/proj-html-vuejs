<template>
    <div id="contacts">
        <!-- <ul>
            <li v-for="(contact, index) in contacts" :key="index">
                <font-awesome-icon :icon="contact.icon" class="icons"/>
                {{ contact.info }}
            </li>
        </ul> -->
        <div class="row" v-for="(contact, index) in contacts" :key="index">
            <div class="col-2">
                <font-awesome-icon :icon="contact.icon" class="icons"/>
            </div>
            <div class="col-10"> {{ contact.info }} </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ContactsComponent',
    data(){
        return {
            contacts: [
                {
                    icon: 'fa-solid fa-globe',
                    info: 'Corporate Location 1600 Lorem ipsum London'
                },
                {
                    icon: 'fa-solid fa-house-chimney',
                    info: 'Residential Location 9521 Lorem ipsum Paddington'
                },
                {
                    icon: 'fa-solid fa-phone-flip',
                    info: '1.800.458.556/1.800.532.2112'
                },
                {
                    icon: 'fa-regular fa-envelope',
                    info: 'info@your-domain.com'
                },
                {
                    icon: 'fa-regular fa-clock',
                    info: 'Monday - Friday 9.00 AM - 6.00 PM'
                },
                {
                    icon: 'fa-regular fa-clock',
                    info: 'Saturday - Sunday 9.00 AM - 12.00 PM'
                }
            ]
        }
    }
}

</script>

<style scoped lang="scss">
  @import '@/assets/styles/pallette.scss';

#contacts{
    .row{
        padding: 5px 0;
        color: $dove-grey-color;
        font-size: 12px;
    }
}
</style>