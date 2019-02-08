<template>
    <div class="section">
        <div class="section"><span>{{ fullname }}</span></div>
        <div class="attribute">
            <img :src="profilePhoto" alt="">
        </div>
        <div class="attribute">
            <a :href="bio" target="_blank"> Biography </a>
        </div>
        <div class="section"><span>{{ `Age: ${ age } years` }}</span></div>

    </div>
</template>

<script>
    export default {
        data() {
            return {
                name: 'Frank',
                lastname: 'Lino',
                birthdate: new Date(1991, 2, 21),
                profilePhoto: 'https://scontent-qro1-1.xx.fbcdn.net/v/t1.0-1/p160x160/21192048_1524308760970131_7522029329401880272_n.jpg?_nc_cat=111&_nc_ht=scontent-qro1-1.xx&oh=9dc8edb125032e5abfc30bd8741685b2&oe=5CB4875D',
                bio: 'https://github.com/Frank712'
            }
        },
        computed: {
            fullname() {
                return `${this.name} ${this.lastname}`;
            },
            age() {
                return this.ageCalculator(this.birthdate);
            }
        },
        methods: {
            ageCalculator( date ) {
                let currentDate = new Date();
                let diff = currentDate - date;
                return Math.floor(diff / (1000 * 60 * 60 * 24 * 365.25));
            }
        }
    }
</script>

<style scoped>
    img {
        border-radius: 50%;
    }
</style>