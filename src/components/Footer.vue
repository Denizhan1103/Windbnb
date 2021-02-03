<template> 
    <div class="footer">
        <div class="footer__line"></div>
        <p class="footer__title">Denizhan @DevChallanges.io</p>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    .footer {
        display: flex;
        height: 100px;
        width: 100%;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        &__line {
            width: 400px;
            height: 0px;
            border: 1px solid #BDBDBD;
        }

        &__title {
            font-weight: 600;
            font-size: 14px;   
            color: #A9A9A9;
        }
    }
</style>