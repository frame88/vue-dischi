<template>
  <div class="search">
      <h3>Choose a genre: </h3>
      <select name="search" v-model="optionValue" @change="$emit('emitSearch', optionValue)" id="search">
          <option value="all">All</option>
          <option value="rock">Rock</option>
          <option value="metal">Metal</option>
          <option value="pop">Pop</option>
          <option value="jazz">Jazz</option>
      </select>
  </div>
</template>

<script>
export default {
    name: 'Search',
    data (){
        return {
            optionValue: "all",
        };
    },
}
</script>

<style lang="scss">
    .search{
        text-align: center;
        padding: 1em 0;
        h3{
        display: inline-block;
        color: lightgray;
        font-size: 1em;
        }
    }
</style>