<template>
  <div>
    <div class="row">
      <div class="col-12">
        <div class="header-img"></div>
      </div>
    </div>

    <div class="row">
      <div class="col-md-7">
        <div class="course h-100">
          <div class="course-header">
            <h2>Course Categories</h2>
            <a href="/">All course</a>
          </div>
        </div>
      </div>

      <div class="col-md-5">
        <div class="row">
          <div class="col-12 d-flex justify-content-center">
            <v-date-picker color="#f7c71b" first-day-of-week="1"></v-date-picker>
          </div>
        </div>

        <div class="row">
          <div class="col-12 d-flex justify-content-center">
            <div class="upcoming">
              <h2 class="title">Upcoming</h2>
              <div class="events">
                <div class="event">
                  <div class="d-flex align-items-center">
                    <img class="img-fluid" src="~assets/image/home/event_24px.png" alt />
                  </div>
                  <div class="pl-3">
                    <p class="event-title">One nation under hate</p>
                    <p class="event-date">3 - 4 SEP 2019</p>
                  </div>
                </div>
                <div class="event">
                  <div class="d-flex align-items-center">
                    <img class="img-fluid" src="~assets/image/home/event_24px.png" alt />
                  </div>
                  <div class="pl-3">
                    <p class="event-title">One nation under hate</p>
                    <p class="event-date">3 - 4 SEP 2019</p>
                  </div>
                </div>
                <div class="event">
                  <div class="d-flex align-items-center">
                    <img class="img-fluid" src="~assets/image/home/event_24px.png" alt />
                  </div>
                  <div class="pl-3">
                    <p class="event-title">One nation under hate</p>
                    <p class="event-date">3 - 4 SEP 2019</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- row -->

    <div class="row bottom-support">
      <div class="col-md-4 border-right">
        <h2 class="feedback-title">Feedback</h2>
        <ul class="pt-4">
          <li>Report complains / suggestions</li>
          <li>System usage questionare for the academic Year 2019</li>
        </ul>
      </div>
      <div class="col-md-4 border-right">
        <h2 class="navigation-title">Navigation</h2>
        <ul class="pt-4">
          <li>Enrollment Code</li>
          <li>All courses</li>
          <li>Request a course</li>
          <li>Learning Portal</li>
          <li>User Manual</li>
        </ul>
      </div>
      <div class="col-md-4">
        <h2 class="help-title">Help & Support</h2>
        <p class="pt-4">
          interest staff opening courses online,
          <a class="text-danger" href="/">click here</a> or contact
          <a class="text-danger" href="mailto:cs@kmitl.ac.th">cs@kmitl.ac.th</a>
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header-img {
  background-image: url("~assets/image/home/cover.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  width: 100%;
  height: 538px;
}

h1,
h2,
h3,
h4,
h5,
h6,
a,
p {
  color: #58595b;
}
p {
  margin-bottom: 0;
}

.course-title {
  justify-content: space-between;
  align-items: baseline;
}
.course-title > a {
  text-decoration: underline;
}

.upcoming {
  width: 100%;
  display: flex;
  flex-direction: column;
  max-width: 300px;
  padding: 12px 10px;
  background-color: white;
  border: 0.5px solid #c1c1c1;
  box-sizing: border-box;
  box-shadow: 3px 4px 4px #c1c1c1;
  border-radius: 5px;
}
.upcoming .title {
  color: #f7c71b !important;
  text-align: center;
  font-size: 30px !important;
}
.upcoming .events {
  display: flex;
  flex-direction: column;
  margin-top: 15px;
}
.upcoming .events .event {
  text-align: center;
  display: flex;
  flex-direction: row;
  margin-bottom: 15px;
  background-color: white;
  padding: 5px 10px;
  box-shadow: 0px 4px 8px rgba(176, 190, 197, 0.24);
  border-radius: 3px;
}
.upcoming .events .event:last-child {
  margin-bottom: 0;
}
.upcoming .events .event .event-title {
  font-size: 16px !important;
  color: #58595b;
  font-weight: bold;
}
.upcoming .events .event .event-date {
  font-size: 12px !important;
  text-align: left;
}

.course {
  display: block;
  border: 0.5px solid #58595b;
  box-sizing: border-box;
  box-shadow: 4px 4px 4px #c1c1c1;
  border-radius: 5px;
  padding: 26px 30px;
}
.course-header {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
}
.course-header a {
  text-decoration: underline;
}

.bottom-support {
  background-color: #f3f3f3;
}

.feedback-title,
.navigation-title,
.help-title {
  position: relative;
  padding-left: 60px;
}
:matches(.feedback-title, .navigation-title, .help-title)::before {
  background-size: cover;
  background-repeat: no-repeat;
  width: 40px;
  height: 40px;
  content: "";
  display: inline-block;
  position: absolute;
  left: 0;
}
.feedback-title::before {
  background-image: url(~assets/image/home/speech-bubbles-comment-option.png);
}
.navigation-title::before {
  background-image: url(~assets/image/home/link-symbol.png);
}
.help-title::before {
  background-image: url(~assets/image/home/information-symbol.png);
}
</style>
