<template>
    <div>
        <head>
            <link href="https://fonts.googleapis.com/css?family=Material+Icons" rel="stylesheet">
        </head>

        <body class='courseBackgroundColor'>
            <div class='courseHeaderContainer'>
                <img class='courseHeaderImg' src='~/assets/CourseHeader.png'>
                <div class='courseHeaderText'>
                    <h1 class='courseHeaderTextSubject'>05506221 Mixed Reality</h1>
                    <h1 class='courseHeaderTextTime'>Friday 09:00 AM - 12:00 PM</h1>
                </div>

                <div class='courseProfileContainer'>
                    <img class='courseProfileImgCrop courseProfileImg' src='~/assets/CourseTeacher.png'>
                    <div class='courseProfileUsername'>
                        <h1 style='font-size: 20px; font-weight: bold;'>Dr. Witchaya Towongpaichayont</h1>
                    </div>
                    <div class='courseProfileDescription'>
                        <v-icon class='courseHomePosition'>home</v-icon>
                        <v-icon class='courseEmailPosition'>email</v-icon>
                        <h1 style='font-size: 18px; font-weight: normal;'>วท. 3105</h1>
                        <h1 style='font-size: 18px; font-weight: normal;'>witchaya.ar@kmitl.ac.th</h1>
                    </div>
                </div>

                <div class ='courseSubjectContainer'>
                    <h1 class='courseSubjectName'>05506221 Mixed Reality</h1>
                    <h1 class='courseSubjectType'>Subject Type : Theory</h1>
                    <h1 class='courseSubjectPrerequisite'>Prerequisite subject : None</h1>
                    <h1 class='courseSubjectCredits'>Credits ( lecture - practice - research )</h1>
                    <h1 class='courseSubjectCreditsNum'>3 ( 3 - 0 - 6 )</h1>
                    <p class='courseSubjectDescription'>
                        <tab1>
                            System theory and concepts, information systems and organizational system,
                            decision support, quality, levels of systems: strategic; tactical;
                            and operational, system components and relationships, information systems strategies,
                            roles of information and information technology : roles of users; developers;
                            and system managers, IS planning and change management, human-computer interface,
                            IS development process, evaluation of IS performance, societal
                            and ethical issues related to information systems design and use.
                        </tab1>
                    </p>

                    <template>
                        <v-row justify="center">
                            <v-btn x-large
                                color="#F8941E"
                                dark
                                @click.stop="dialog = true"
                                class="courseSubjectBtnPosition"
                            >
                                Get Access
                            </v-btn>

                            <v-dialog v-model="dialog" max-width="600">
                                <v-card color="#FFFFFF" dark>
                                   <span class="material-icons courseSubjectDialogWarning">error_outline</span>

                                    <v-card-text>
                                        <p class="courseSubjectDialogText"><center><br>Are you sure to access</center></p>
                                        <p class="courseSubjectDialogText"><center><br>Mixed Reality course?</center></p>
                                    </v-card-text>

                                    <v-card-actions>
                                        <v-spacer></v-spacer>

                                        <v-btn x-large
                                            color="#FE7065"
                                            dark
                                            @click="dialog = false"
                                            class="courseSubjectDialogBtnNo"
                                        >
                                            NO
                                        </v-btn>

                                        <v-btn x-large
                                            color="#BAD26E"
                                            dark
                                            @click="dialog = false"
                                            class="courseSubjectDialogBtnYes"
                                        >
                                            YES
                                        </v-btn>
                                    </v-card-actions>
                                </v-card>
                            </v-dialog>
                        </v-row>
                    </template>
                </div>
            </div>
        </body>
    </div>
</template>

<style>
.courseBackgroundColor {
    background-color: #F3F3F3;
}

.courseHeaderContainer {
    position: relative;
    display: inline-block;
    width: 100%;
    margin-top: 80px;
}

.courseHeaderImg {
    display: block;
    width: 100%;
    height: 247px;
    margin: auto;
    padding: auto;
}


@media only screen and (min-width: 1024px) and (max-width: 1200px){
    .courseHeaderImg {
        display: block;
        width: 100%;
        height: 217px;
        margin: auto;
        padding: auto;
    }
}

.courseHeaderText {
    position: absolute;
    margin-top: 65px;
    margin-right: 100px;
    text-align: right;
    height: 30%;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    color: white;
}

@media only screen and (min-width: 1024px) and (max-width: 1200px){
    .courseHeaderText {
        position: absolute;
        margin-top: 65px;
        margin-right: 90px;
        text-align: right;
        height: 30%;
        top: 0;
        bottom: 0;
        right: 0;
        left: 0;
        color: white;
    }
}

.courseHomePosition {
    position: absolute;
    margin-top: 2px;
    margin-left: -40px;
}

.courseEmailPosition {
    position: absolute;
    margin-top: 27px;
    margin-left: -40px;
}

.courseHeaderTextSubject {
    font-size: 64px;
    font-weight: bold;
}

@media only screen and (min-width: 1024px) and (max-width: 1200px){
    .courseHeaderTextSubject {
        font-size: 44px;
        font-weight: bold;
    }
}

.courseHeaderTextTime {
    font-size: 24px;
    font-weight: normal;
}

@media only screen and (min-width: 1024px) and (max-width: 1200px){
    .courseHeaderTextTime {
        font-size: 22px;
        font-weight: normal;
    }
}

.courseProfileContainer {
    position: relative;
    display: inline-block;
    width: 360px;
    height: 434px;
    margin-top: 53px;
    margin-left: 390px;
    background: #FFFFFF;
    box-shadow: 1px 2px 4px rgba(0, 0, 0, 0.2);
    border-radius: 5px;

    color: #58595B;
}

@media only screen and (min-width: 1024px) and (max-width: 1200px){
    .courseProfileContainer {
        position: relative;
        display: inline-block;
        width: 360px;
        height: 434px;
        margin-top: 53px;
        left: -5%;
        /* margin-left: 390px; */
        background: #FFFFFF;
        box-shadow: 1px 2px 4px rgba(0, 0, 0, 0.2);
        border-radius: 5px;

        color: #58595B;
    }
}

.courseProfileImgCrop {
    object-fit: cover
}

.courseProfileImg {
    display: block;
    width: 150px;
    height: 150px;
    margin: auto;
    margin-top: 59px;
    border-radius: 50%;
}

.courseProfileUsername {
    position: relative;
    margin-top: 31px;
    text-align: center;
}

.courseProfileDescription {
    position: relative;
    margin-top: 45px;
    margin-left: 105px;
}

.courseSubjectContainer {
    position: absolute;
    display: inline-block;
    width: 780px;
    height: 660px;
    margin-top: 53px;
    margin-left: 60px;
    margin-bottom: 50px;
    background: #FFFFFF;
    box-shadow: 1px 2px 4px rgba(0, 0, 0, 0.2);
    border-radius: 5px;

    color: #58595B;
}

@media only screen and (min-width: 1024px) and (max-width: 1200px){
    .courseSubjectContainer {
        position: absolute;
        display: inline-block;
        width: 780px;
        height: 660px;
        margin-top: 530px;
        margin-left: -630px;
        margin-bottom: 50px;
        background: #FFFFFF;
        box-shadow: 1px 2px 4px rgba(0, 0, 0, 0.2);
        border-radius: 5px;

        color: #58595B;
    }
}

.courseSubjectName {
    position: absolute;
    margin-top: 69px;
    margin-left: 63px;
    font-size: 28px;
    font-weight: bold;
}

.courseSubjectType {
    position: absolute;
    margin-top: 69px;
    margin-left: 525px;
    font-size: 20px;
    font-weight: bold;
}

.courseSubjectPrerequisite {
    position: absolute;
    width: 252px;
    height: 53px;
    margin-top: 116px;
    margin-left: 476px;
    font-size: 20px;
    font-weight: bold;
}

.courseSubjectCredits{
    position: absolute;
    margin-top: 155px;
    margin-left: 379px;
    font-size: 20px;
    font-weight: bold;
}

.courseSubjectCreditsNum{
    position: absolute;
    margin-top: 185px;
    margin-left: 611px;
    font-size: 20px;
    font-weight: bold;
}

.courseSubjectDescription {
    position: absolute;
    margin-top: 274px;
    margin-left: 53px;
    margin-right: 49px;
    font-size: 20px;
    font-weight: normal;
}

.courseSubjectBtnPosition {
    position: absolute;
    width: 247.23px;
    /*height: 58px;     Unfortunately, v-button is not allowed to manually adjust height as it depends on the size we selected*/
    margin-top: 542px;
    margin-left: 473px;

    border-radius: 5px;

    font-size: 24px;
    font-weight: bold;
}

/*Temporary fix for v-dialog bug (dialog does not display after pressing button)*/
.v-dialog__container {
    display: unset;
}

/*Rules for sizing and coloring the warning icon
  Important: Icon class declaration must begin w/ material-icons
  Information: http://google.github.io/material-design-icons*/
.material-icons.courseSubjectDialogWarning {
    margin-top: 20px;
    margin-left: 260px;
    font-size: 85px;
    color: #F8941E;
}

.courseSubjectDialogText {
    font-size: 26px;
    font-weight: bold;
    color: #58595B;
}

.courseSubjectDialogBtnNo {
    width: 150px;
    margin-top: 35px;
    margin-right: 50px;
    margin-bottom: 20px;
}

.courseSubjectDialogBtnYes {
    width: 150px;
    margin-top: 35px;
    margin-right: 116px;
    margin-bottom: 20px;
}

tab1 {
    padding-left: 4em;
}

tab2 {
    padding-left: 8em;
}

tab3 {
    padding-left: 12em;
}

*{
    font-family: Roboto;
}
</style>

<script>
  export default {
    data () {
      return {
        dialog: false,
      }
    },
  }
</script>
