<template>
    <div class="entrance">
        <span>Entrance</span>
        <client/>
        <div class="section">
            Section
        </div>
    </div>
</template>

<script>
    import Client from '@/components/Client.vue';

    export default {
        components: { Client }
    }
</script>

<style>
    .entrance {
        margin: 10px;
        padding: 10px;
        background-color: #553f75;
        font-size: 2.6rem;
    }
    .section {
        font-size: 2.4rem;
        color: #020202;
        background-color: #e3e993;
        border-radius: 5px;
        margin: 10px;
        padding: 10px;
    }
</style>