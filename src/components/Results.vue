<template>
    <div class="result-block">
        <p>Reaction Time - {{ score }} ms</p>
        <h1 class="rank">{{ rank }}</h1>
    </div>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 350) {
            this.rank = 'That was fast!'
        } else if (this.score < 600) {
            this.rank = 'Good Reflexes'
        } else {
            this.rank = 'Very Slow pace...'
        }
    }
}
</script>

<style lang="css">
    
.result-block {
    color: #0192a5;
}

.rank {
    font-size: 1.4rem;
    color: #0192a5;
    font-weight: bold;
}

</style>