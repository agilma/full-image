<template>
  <div class="body">
    <b-row class="gallery">
      <b-col>
        <b-carousel id="carousel1"
          :interval="4000"
        >
        <b-carousel-slide v-for="image in lefttop" :key="image.id" v-bind:img-src="image">
        </b-carousel-slide>
        </b-carousel>
      </b-col>
      <b-col>
        <b-card-img colspan="2" class="right" src="P1.jpg"/>
      </b-col>
    </b-row>

    <b-row>
      <b-col>
         <b-carousel id="carousel1"
          :interval="4000"
        >
        <b-carousel-slide v-for="image in leftbottom" :key="image.id" v-bind:img-src="image">
        </b-carousel-slide>
        </b-carousel>
      </b-col>
      <b-col>
      </b-col>
    </b-row>
  
    <div class="footer">
        <b-row>
          <b-col class="text-right">
            <b-card-img class="logo" :src="logo"/>
          </b-col>
          <b-col class="about">
            <b>{{web}}</b>
            <br>{{alamat}}
            <br> {{jam}}
          </b-col>     
        </b-row>
    </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      lefttop: [ 'l2.jpg', 'l3.jpg' , 'l4.jpg'],
      leftbottom : ['f1.jpg','f2.png','f3.jpg'],
      logo : ['logo.png'],
      web: 'Kopibatu@gmail.com',
      alamat : 'Jalan Kilimanjaro no 25, Batu',
      jam : 'Setiap Hari 08.00-21.00'
    }
  }, 
}
</script>

<style scoped>
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
  height: 100px;
  bottom: 0;
  width: 100%;
  background: rgb(53, 50, 50);
  padding-top: 0.5%;
}
.logo{
  width: 75px;
  height: 75px;
}
.about{
  font-size: medium;
  color:white;
}
</style>