<template>
  <div class="wrapper">
    <div class="wrapper-tap">
      <div class="row justify-content-md-center">
        <div class="col-md-auto body">
          <a href="">
            <h1 class="black bold">
              Todo
            </h1>
          </a>
        </div>
        <div class="col col-lg-1 body">
          <a href="./done">
            <h1 class="black bold">
              Done
            </h1>
          </a>
        </div>
      </div>
    </div>

    <br/>
    <br/>
    <br/>
    <br/>

    <v-card
      class="mx-auto"
      width="1500"
      min-height="800"
    >

      <div class="dropdown posi-dropdown">
        <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          All classes
        </button>
        <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
          <a class="dropdown-item" href="#">Action</a>
          <a class="dropdown-item" href="#">Another action</a>
          <a class="dropdown-item" href="#">Something else here</a>
        </div>
      </div>

      <div class="center">
        <div class="card" v-for="post in filteredList" >
          <a target="_blank" class="left">
            <h3 class="bold">{{ post.title }}</h3>
            <h8 class="bold detail C58595b">{{post.sub}} &emsp; &emsp;</h8>
            <h8 style="color:#B6B6B6;">{{post.date}}</h8>
          </a>
        </div>
      </div>

    </v-card>
    <br/>
    <br/>
    <br/>
    <br/>
    <br/>
  </div>
</template>

<style scoped>
.wrapper {
  background-color: #E5E5E5;
  min-height: calc(1200px);
  width: 100%;
}

.wrapper-tap {
  position: relative;
  display: inline-block;
  background-color: #FFFFFF;
  width: 100%;
  margin-top: 80px;
  height: 112px;
}

.html, .body {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  margin-top: 50px;
}

.center {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.posi-dropdown {
  display: inline-block;
  padding-top: 60px;
  padding-left: 50px;
}

.center-btn {
  position: relative;
  top: 5px;
}

.card {
   box-shadow: rgba(0, 0, 0, 0.117647) 0px 1px 6px, rgba(0, 0, 0, 0.117647) 0px 1px 4px;
   width: 1200px;
   margin: 36px;
   min-height: 150px;
   max-height: 300px;
   background: linear-gradient(to right, #B39DDB 0%,#B39DDB 1%,#B39DDB 1%,white 1%,white 100%);
   transition: .15s all ease-in-out;
   :hover {
     transform: scale(1.1);
   }
 }

.left{
  text-align: left;
  padding-top: 40px;
  padding-left: 40px;
}
</style>

<script>
class Post {
  constructor(title, sub, date) {
    this.title = title;
    this.sub = sub;
    this.date = date;
  }
}
import "@/css/font.css";
export default{
  css: 'font',
  data() {
    return {
      search: "",
      postList: [
        new Post(
          'Use case OX game',
          'Mixed Reality',
          '- Due Aug 16 2018, 11.59 PM'
        ),
        new Post(
          'ASS2',
          'Mixed Reality',
          '- Due Aug 16 2018, 11.59 PM'
        ),
        new Post(
          'ASS3',
          'Mixed Reality',
          '- Due Aug 16 2018, 11.59 PM'
        )
      ]
    }
  },
  computed: {
  filteredList() {
    return this.postList.filter(post => {
      return post.title.toLowerCase().includes(this.search.toLowerCase())
      })
    }
  }
}
</script>
