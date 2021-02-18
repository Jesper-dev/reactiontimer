<template>
  <p>Your reaction time is: {{ score }} ms</p>
  <p class="rank">Your rank is: {{rank}}</p>
</template>

<script>
export default {
    data() {
        return {
            rank: null
        }
    },
    props: {
        'score': Number
    },
    mounted() {
        if(this.score < 250){
            this.rank = 'Ninja fingers'
        } else if (this.score < 400) {
            this.rank = 'Rapid reflexes'
        } else {
            this.rank = 'Snail pace...'
        }
    }
}
</script>

<style scoped>
    .rank {
        font-size: 1.4rem;
        color: #0faf87;
        font-weight: bold;
    }
</style>