<template>
    <div class="ad">
        <span>{{ presentations[index] }}</span>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                presentations: [
                    'Hamilton - 20:30',
                    'Frozen - 15:00',
                    'Anastacia - 14:00',
                    'El rey Leon - 22:00'
                ],
                index : 0
            }
        },
        methods: {
            showAd() {
                this.index++;
                if( this.index === this.presentations.length ) {
                    this.index = 0;
                    this.$destroy();
                }
            }
        },
        beforeCreate(){
            console.log('beforeCreate()');
        },
        created() {
            console.log('created()');
        },
        beforeMount() {
            console.log('beforeMount()');
        },
        mounted() {
            console.log('mounted()');
            setInterval(this.showAd, 2000);
        },
        beforeUpdate() {
            console.log('beforeUpdated()');
        },
        updated() {
            console.log('updated()');
        },
        beforeDestroy() {
            console.log('beforeDestroy()');
        },
        destroyed() {
            console.log('destroyed()');
        }

    }
</script>

<style>
    .ad {
        margin: 10px;
        font-size: 2rem;
        border-top-color: white;
        border-top-width: 1px;
        border-top-style: solid;

        border-bottom-color: white;
        border-bottom-width: 1px;
        border-bottom-style: solid;
    }
</style>