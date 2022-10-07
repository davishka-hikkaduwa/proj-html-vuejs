<template>
    <div class="title-container">
        <h5 class="custom-underline">{{ title }}</h5>
    </div>
</template>

<script>
export default {
    name: 'SectionTitleComponent',
    props: {
        title: String,
    },
}
</script>

<style scoped lang="scss">
    // ----- TEXT-UNDERLINE -----
    .custom-underline {
        padding-bottom: 20px;
        position: relative;
    }

    .custom-underline::before {
        content: '';
        position: absolute;
        bottom: 0;
        left: 40%;
        width: 140px;
        height: 2px;
        background-color: #f9d03f;
    }
    // ----- /TEXT-UNDERLINE -----
</style>