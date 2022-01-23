<template>
  <div class="col-2 m-3 p-3 text-center border-0 card">
        <img class="mb-3" :src="card.poster" alt="">
        <h2>{{card.title}}</h2>
        <h3>{{card.author}}</h3>
        <h4>{{card.year}}</h4>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: ['card'],
}
</script>

<style lang="scss" scoped>
    .card{
        border-radius: 0px;
        background-color: #2E3A46;
        h2{
            color: white;
            font-size: 1.5em;
        }
        h3, h4{
            color: lightgray;
            font-size: 1em;
        }
    }
</style>