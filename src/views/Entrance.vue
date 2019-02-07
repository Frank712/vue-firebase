<template>
    <div class="entrance">
        <ad/>
        <client/>
    </div>
</template>

<script>
    import Client from '@/components/Client.vue';
    import Ad from '@/components/Ad.vue';

    export default {
        components: { Client, Ad }
    }
</script>
