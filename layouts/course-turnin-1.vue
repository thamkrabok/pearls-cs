<template>
  <div class="wrapper">
    <div class="wrapper-tap">
      <div class="row justify-content-md-center">
        <div class="col-md-auto body">
          <a href="">
            <h1 class="black bold">
              Instructions
            </h1>
          </a>
        </div>
      </div>
    </div>

    <div class='courseHeaderContainer-turn'>
      <img class='courseHeaderImg' src='~/assets/CourseHeader.png'>
      <div class='courseHeaderText'>
        <h1 class='courseHeaderTextSubject'>05506221 Mixed Reality</h1>
        <h1 class='courseHeaderTextTime'>Friday 09:00 AM - 12:00 PM</h1>
      </div>
    </div>

    <v-card
      class="mx-auto margin-box"
      width="1500"
      min-height="600"
    >
      <v-avatar size="60" class="avatar" style="border-radius:150px;">
        <img
          src="https://cdn.vuetifyjs.com/images/john.jpg"
          alt="John"
        >
      </v-avatar>
      <h6 class="bold C58595b posi-name-teach">{{post.teachname}}</h6>
      <h7 class="C58595b posi-name-teach">{{post.date}}</h7>
      <h8 class="C58595b bold posi-point">{{post.point}}  &nbsp; Point</h8>
      <h8 class="bold C58595b posi-name-teach posi-assign-text">{{post.assign}}</h8>
      <img src="@/assets/assignment.svg" class="posi-assign">
      <h8 class="C58595b posi-name-teach posi-date">Due {{post.date}}</h8>

      <hr style="border: 1px solid #f8941e"/>

      <h8 class="C58595b bold posi-name-teach" style="display:flex;padding-top:30px;">Class comment</h8>
      <v-avatar size="60" class="avatar-2" style="border-radius:150px;">
        <img
          src="https://cdn.vuetifyjs.com/images/john.jpg"
          alt="John"
        >
      </v-avatar>
      <form>
        <div class="form-group">
          <textarea name="comment" placeholder="Add comment class" class="form-control posi-comment" rows="3"></textarea>
        </div>
        <v-btn depressed large color="#f8941e" class="posi-btn"><a style="color:#FFFFFF;">+ Your work</a></v-btn>
      </form>

    </v-card>
  </div>
</template>

<style scoped>
.posi-btn {
  position: relative;
  right: -1280px;
  top: -70px;
}
.wrapper {
  background-color: #E5E5E5;
  min-height: calc(1400px);
  width: 100%;
}

.wrapper-tap {
  position: relative;
  display: inline-block;
  background-color: #FFFFFF;
  width: 100%;
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

.courseHeaderContainer-turn {
    position: relative;
    display: inline-block;
    width: 100%;
}

.margin-box {
  margin-top: 80px;
}

.avatar {
  display: flex;
  padding-left: 100px;
  top: 50px;
}

.avatar-2 {
  display: flex;
  padding-left: 180px;
  padding-top: 50px;
}

.posi-name-teach {
  display: flex;
  padding-left: 150px;
}

.posi-point {
  position: relative;
  display: flex;
  padding-left: 1350px;
  top: -55px;
}

.posi-assign {
  position: relative;
  padding-left: 70px;
  top: -40px;
}

.posi-assign-text {
  display: flex;
  padding-top: 30px;
}

.posi-date {
  position: relative;
  top: -40px;
}

.posi-comment {
  position: relative;
  left: 230px;
  top: -16px;
  width: 750px;
  height: 50px;
  border-color: #FFFFFF;
}
</style>

<script>
class Post {
  constructor(teachname,stuname,subject,date,point,assign){
    this.teachname = teachname;
    this.stuname = stuname;
    this.subject = subject;
    this.date = date;
    this.point = point;
    this.assign = assign;
  }
}
import "@/css/font.css";
export default{
  css: 'font',
  data() {
    return {
      post:
        new Post(
          'Witchaya Towongpaichayont',
          'Piyawat Sawong',
          'Mixed Reality',
          'May 4, 2019 (Edited May 11, 2019)',
          '15',
          'new assignment : Quest 030 : AR in your Area (2)'
        ),
      search: "",
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
