<template>
  <Cards :photo="returnPhotos()" @my-event="changeAnimal"/>
</template>

<script>
import Cards from "@/components/10.22/2task/Cards";

export default {
  name: "Main_3",
  components: {
    Cards
  },
  data() {
    return {
      cats: [
        "https://images.theconversation.com/files/350865/original/file-20200803-24-50u91u.jpg?ixlib=rb-1.1.0&q=45&auto=format&w=320&h=213&fit=crop",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRWO_UAe27eAhTik2ggPbzKGQfuXD1oVosA_Q&usqp=CAU",
        "https://www.balticdentists.com/wp-content/uploads/2019/08/cat-pet-animal-domestic-104827.jpeg",
        "https://ichef.bbci.co.uk/news/976/cpsprodpb/41CF/production/_109474861_angrycat-index-getty3-3.jpg",
        "https://thumbs-prod.si-cdn.com/d4e3zqOM5KUq8m0m-AFVxuqa5ZM=/800x600/filters:no_upscale():focal(554x699:555x700)/https://public-media.si-cdn.com/filer/a4/04/a404c799-7118-459a-8de4-89e4a44b124f/img_1317.jpg"
      ],
      dogs: [
        "https://img.webmd.com/dtmcms/live/webmd/consumer_assets/site_images/article_thumbnails/other/dog_cool_summer_slideshow/1800x1200_dog_cool_summer_other.jpg",
        "https://i.ytimg.com/vi/MPV2METPeJU/maxresdefault.jpg",
        "https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/golden-retriever-royalty-free-image-506756303-1560962726.jpg?crop=0.672xw:1.00xh;0.166xw,0&resize=640:*",
      ],
      whatToSend:'cat'
    }
  },
  methods: {
    changeAnimal(animal) {
      this.whatToSend = animal
    },
    returnPhotos(){
      if(this.whatToSend === 'cat'){
        return this.cats
      } else{
        return this.dogs
      }
    }
  }
}
</script>

<style scoped>

</style>