<template>
  <div class="body">
    <b-row class="gallery">
      <b-col>
        <b-carousel id="carousel1"
          :interval="4000"
        >
          <b-carousel-slide 
            v-for="(img,i) in data.slider" 
            :key="i" 
            v-bind:img-src="img.image"
          />
        </b-carousel>
      </b-col>
    </b-row>
  
    <div class="footer">
        <b-row class="py-3 align-items-center">
          <b-col class="text-right">
            <b-card-img class="logo" :src="data.company.logo"/>
          </b-col>
          <b-col class="about">
            <p class="title mb-1">{{ data.company.name }}</p>
            <p class="content mb-0">{{ data.company.email }}</p>
            <p class="content mb-0">{{ data.company.address }}</p>
            <p class="content mb-0">{{ data.company.open }}</p>
          </b-col>     
        </b-row>
    </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      data: require('~/json/app.json'),
    }
  }, 
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Mono:wght@400;500&family=Raleway:wght@300&display=swap');

.body{
  overflow: hidden;
  background: black;
  height: 100vh;
}
.gallery{
  height : 41vh;
}
.right{
  height: 925px;
}
.footer{
  position: fixed;
  height: 120px;
  bottom: 0;
  width: 100%;
  background: rgba(30, 29, 29, .27);
}
.logo{
  width: 75px;
  height: 75px;
}
.about{
  font-size: medium;
  color:white;
}
.title {
  font-family: 'Noto Sans Mono', monospace;
  font-weight: bold;
  font-size: 1rem;
}
.content {
  font-family: 'Raleway', sans-serif;
  font-size: .9rem;
}
</style>