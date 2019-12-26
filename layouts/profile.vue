<template>
<body class="Ce5e5e5">
  <div class="wrapper-profile">

    <div class="panel panel-default background-f8941e">
      <v-avatar size="250" class="avatar">
        <img
          src="https://cdn.vuetifyjs.com/images/john.jpg"
          alt="John"
        >
      </v-avatar>
      <h1 class="white bold size-50 profile-name">Mr.Piyawat Sawong</h1>
      <h3 class="white profile-id">Student ID : 60050123</h3>
      <h3 class="white bold profile-ad-date">Date of Admission : 2016</h3>
      <h3 class="white bold profile-grade-date">Date of Graduation : N/A (Status : Study)</h3>
      <div class="my-2 btn-edit">
        <v-btn>
          Edit
          <div class="mx-1"></div>
          <v-icon>mdi-pencil</v-icon>
        </v-btn>
      </div>
    </div>

    <div class="box-main-content">
    <v-row>
      <v-col cols="8" sm="5">
        <v-card
          class="mx-auto"
          max-width="400"
          tile
          min-height="720"
        >
          <v-list flat>
            <v-subheader class="box-content"><h1 class="bold" style="color: #E2683C">SKILLS</h1></v-subheader>
            <hr>
            <v-list-item-group v-model="item" color="primary">
              <v-list-item
                v-for="(item, i) in items"
                :key="i"
              >
                <v-list-item-icon class="item-content-1">
                  <v-icon v-text="item.icon"></v-icon>
                </v-list-item-icon>
                <v-list-item-content class="item-content-2 C58595b">
                  <v-list-item-title style="font-size:30px" v-text="item.text"></v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-card>
      </v-col>

      <v-col cols="10" sm="6" >
        <v-card
          class="mx-auto"
          max-width="1050"
          tile
          min-height="200"
        >
          <v-list flat>
            <v-subheader class="box-content"><h1 class="bold" style="color: #E2683C">CERTIFICATE</h1></v-subheader>
            <hr>
            <v-list-item-group v-model="item" color="primary">
              <v-list-item
                v-for="(item, i) in items"
                :key="i"
              >
                <v-list-item-icon class="item-content-1">
                  <v-icon v-text="item.icon"></v-icon>
                </v-list-item-icon>
                <v-list-item-content class="item-content-2 C58595b">
                  <v-list-item-title style="font-size:30px" v-text="item.text"></v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-card>

        <br/>
        <br/>

        <v-card
          class="mx-auto"
          max-width="1050"
          tile
          min-height="350"
        >
          <v-list flat>
            <v-subheader class="box-content"><h1 class="bold" style="color: #E2683C">TRACK RECORD</h1></v-subheader>
            <hr>
            <v-list-item-group v-model="item" color="primary">
              <v-list-item
                v-for="(item, i) in items"
                :key="i"
              >
                <v-list-item-icon class="item-content-1">
                  <v-icon v-text="item.icon"></v-icon>
                </v-list-item-icon>
                <v-list-item-content class="item-content-2 C58595b">
                  <v-list-item-title style="font-size:30px" v-text="item.text"></v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-card>

      </v-col>

    </v-row>

  </div>

  </div>
</body>
</template>

<style scoped>
.Ce5e5e5{
  background-color: #E5E5E5;
  min-height: 1300px;
  max-height: 3000px;
}

.wrapper-profile {
  position: absolute;
  padding-top: 50px;
  width: 100%;
}

.panel {
  position: relative;
  min-height: 350px;
}

.avatar {
  display: flex;
  padding-left: 350px;
  top: 50px;
}

.profile-name {
  display: flex;
  margin-top: -150px;
  padding-left: 29%;
}

.profile-id {
  display: flex;
  margin-top: 10px;
  padding-left: 29%;
}

.profile-ad-date {
  display: flex;
  margin-top: 100px;
  padding-left: 29%;
}

.profile-grade-date {
  display: flex;
  margin-top: -40px;
  padding-left: 65%;
}

.btn-edit {
  position: absolute;
  top: 35px;
  left: 86%;
}

.box-main-content {
  padding-top:70px;
}

.box-content{
  padding-top:50px;
  padding-left:37px;
}

.item-content-1 {
  padding-top:5px;
  padding-left:50px;
}

.item-content-2 {
padding-top:15px;
padding-left:15px;
}

@media only screen and (min-width: 320px) and (max-width: 419px) {

}

@media only screen and (min-width: 1024px) and (max-width: 1200px){
  .Ce5e5e5{
    background-color: #E5E5E5;
    min-height: 1300px;
    max-height: 3000px;
  }

  .box-main-content {
    padding-top: 70px;
    padding-left: 80px;
  }

}

@media only screen and (min-width: 1200px) and (max-width: 1366px){
  .Ce5e5e5{
    background-color: #E5E5E5;
    min-height: 1400px;
    max-height: 3000px;
  }
}


</style>

<script>
  export default {
    data: () => ({
      item: 1,
      items: [
        { text: 'Real-Time', icon: 'mdi-clock' },
        { text: 'Audience', icon: 'mdi-account' },
        { text: 'Conversions', icon: 'mdi-flag' },
      ],
    }),
  }
</script>
