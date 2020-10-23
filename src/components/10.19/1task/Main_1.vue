<template>
  <Header></Header>
  <div class="d-flex">
    <VerticalCard :image="items[0].photo" :text="items[0].text"/>
    <VerticalCard :image="items[1].photo" :text="items[1].text"/>
  </div>

  <HorizontalCard :image="items[2].photo" :text="items[2].text"/>
  <HorizontalCard :image="items[3].photo" :text="items[3].text"/>

</template>

<script>
import Header from "@/components/10.19/1task/Header";
import VerticalCard from "@/components/10.19/1task/VerticalCard";
import HorizontalCard from "@/components/10.19/1task/HorizontalCard";

export default {
  name: "Main_1",
  components: {
    VerticalCard,
    HorizontalCard,
    Header,
  },
  data() {
    return {
      items: [
        {
          photo: "https://g4.dcdn.lt/images/pix/280x170/UPVynmOG5Uk/grumpy-cat-76998943.jpg",
          text: "mm very beautiful cat, i would like to pet it"
        },
        {
          photo: "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcS5Bm3mL68X5kZ4QEpSm1nIHN6qxSfsRhREyg&usqp=CAU",
          text: "also cool cat, i saw it one on the street"
        },
        {
          photo: "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcS2cR2u7bmtIyMOCTkbpvEZB83-swiUZFm1NQ&usqp=CAU",
          text: "nepersaunamas ragelis, visiems gyvenimo atvejams"
        },
        {
          photo: "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTwxU5WuIx0dnvEi83DUc_x4McFI6eLAYdLeg&usqp=CAU",
          text: "statybu sezonas atidarytas"
        },
      ]
    }
  }

}
</script>

<style scoped>

</style>