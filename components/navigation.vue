<template>
  <div>
    <nav class="navbar navbar-expand-lg">
      <div v-if="!$store.state.article.title" class="container">
        <img class="navbar-brand" href="#" src="https://static.foxnews.com/static/orion/styles/img/fox-business/s/logos/fox-business-2-color.svg"/>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item active">
              <a class="nav-link" href="#">Personal Finance<span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Economy</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Markets</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Watchlist</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Lifesyle</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Real Estate</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Tech</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">TV</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Podcasts</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">More</a>
            </li>
          </ul>
        </div>
      </div>
      <div v-else class="container">
        <a class="navbar-brand" href="#" @click="goBack()">
          <span class="ion-android-arrow-back"></span>
        </a>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  methods : {
    goBack () {
      this.$store.commit('setArticle', {})
      this.$router.replace({ 'path' : '/' })
    }
  }
}
</script>

<style lang="scss" scoped>
.navbar-brand {
  span {
    font-size: 32px;
  }
}
