<template>
    <div class="section">
        <div class="section"><span>{{ fullname }}</span></div>
        <div class="section"><span>{{ `Age: ${ age } years old` }}</span></div>

    </div>
</template>

<script>
    export default {
        data() {
            return {
                name: 'Frank',
                lastname: 'Lino',
                birthdate: new Date(1991, 2, 21)
            }
        },
        computed: {
            fullname() {
                return `${this.name} ${this.lastname}`;
            },
            age() {
                let currentDate = new Date();
                let diff = currentDate - this.birthdate;
                return Math.floor(diff / (1000 * 60 * 60 * 24 * 365.25));
            }
        }
    }
</script>

<style scoped>
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