<template>
  <div class="ras">
    <carousel v-bind:carousel="data['carousel']"/>
    <about-us v-bind:data="data['about']" v-bind:img="img" />
    <team v-bind:data="data['team']"/>
  </div>
</template>

<script>
import Database from '/database/database';
import AboutUs from '@/components/committees/AboutUs';
import Carousel from '@/components/committees/Carousel';
import Team from '@/components/committees/Team';

export default{

  components:{
    'about-us':AboutUs,
    'carousel':Carousel,
    'team':Team,
  },

  data(){
    return{
      data: Database.committees.ras,
      img:require('../components/committees/'+Database.committees.ras.img)


    }
  }
}

</script>
