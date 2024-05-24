<script>
export default {
  data() {
    return {
      links: [
        {
          text: "CHARACTERS",
          url: "#CHARACTERS",
        },
        {
          text: "COMICS",
          url: "#COMICS",
        },
        {
          text: "MOVIES",
          url: "#MOVIES",
        },
        {
          text: "TV",
          url: "#TV",
        },
        {
          text: "GAME",
          url: "#GAME",
        },
        {
          text: "COLLECTIBLES",
          url: "#COLLECTIBLES",
        },
        {
          text: "VIDEOS",
          url: "#VIDEOS",
        },
        {
          text: "FANS",
          url: "#FANS",
        },
        {
          text: "NEWS",
          url: "#NEWS",
        },
        {
          text: "SHOP",
          url: "#SHOP",
        },
      ],
    }
  },
  methods:{
        getImg(percorso){
            let risultato = new URL('../assets/' + percorso, import.meta.url);
            return risultato.href
        }
    }
}
</script>

<template>

  <header>

    <div class="container">

      <div class="row">
        <div class="col"><img src="../assets/dc-logo.png" width="50px"></div>
        <div class="col d-flex align-items-center">
          <a v-for="link in links" :href="link.url">{{ link.text }}</a>
        </div>
      </div>

    </div>

  </header>

</template>

<style scoped>
header {
  background-color: white;
  padding: 1rem;
}

a {
  color: black;
  text-decoration: none;
  padding: 0 0.5rem;
}
</style>
