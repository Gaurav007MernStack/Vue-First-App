<template>
  <p>Reaction Time - {{ score }} ms </p>
  <p class="rank">{{ rank }} </p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return{
            rank: null
        }
    },
    mounted() {
        if (this.score < 350){
            this.rank = "Super Fast"
        } else if (this.score < 500 ){
            this.rank = 'Intermediate, can do Better'
        } else {
            this.rank = 'Slow ...'
        }
    }
}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>