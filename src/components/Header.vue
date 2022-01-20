<template>
  <header>
      <div class="container-max">
        
              <div class="container-logo">
                   <!--     {{ logo }}       -->
              </div>
        
      </div>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.container-max {
    height: 10vh;
    background-color: red;
    display: flex;
    align-items: center;
}

.container {
    display: flex;
    height: 10vh;
}

.container-logo {
    width: 60px;
    height: 60px;
    background-color: yellow;
    align-self: center;
    border: 2px solid green;
    border-radius: 50%;
    margin-left: 3em;
}


</style>