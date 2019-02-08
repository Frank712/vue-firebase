<template>
    <div class="section">
        <div class="attribute">
            <span class="tickets"> {{tickets}} </span>
        </div>
        <div class="attribute">
            <button @click="updateCount(+1)">+</button>
            <button @click="updateCount(-1)">-</button>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                tickets: 0
            }
        },
        methods: {
            updateCount( count ){
                this.tickets += count;
                if( this.tickets > 10 )
                    this.tickets = 10;
                else if ( this.tickets < 0 )
                    this.tickets = 0;
            }
        }
    }
</script>

<style>
    .tickets {
        font-size: 3.75rem;
        font-weight: bold;
    }
</style>