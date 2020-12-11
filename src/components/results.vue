<template>
  <p>Reaction Time: {{score}} ms</p>
  <p class="rank">{{rank}}</p>
</template>

<script>
export default {
    props:['score'],
    data(){
        return{
            rank:null,
        }
    },
    mounted(){
        if(this.score < 250){
            this.rank = 'Fastest triggers in the wild wild west!'
        }else if(this.score < 400){
            this.rank = 'Mediocre results for a mediocre man.'
        }else{
            this.rank = 'Your Dead....'
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