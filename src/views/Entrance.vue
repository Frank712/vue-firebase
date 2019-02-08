<template>
    <div class="entrance">
        <ad/>
        <client/>
        <email/>
        <tickets/>
        <signature/>
    </div>
</template>

<script>
    import Client from '@/components/Client.vue';
    import Ad from '@/components/Ad.vue';
    import Tickets from '@/components/Tickets.vue';
    import Signature from '@/components/Signature.vue';
    import Email from '@/components/Email.vue';

    export default {
        components: { Client, Ad, Tickets, Signature, Email }
    }
</script>

<style>
    .section {
        font-size: 2.4rem;
        color: #020202;
        background-color: #e9e9e9;
        border-radius: 5px;
        margin: 10px;
        padding: 10px;
    }

    .attribute {
        margin: 10px;
    }
</style>