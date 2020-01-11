<template>
  <div class="wrapper">
    <div class="wrapper-tap">
      <div class="row justify-content-md-center">
        <div class="col-md-auto body">
          <a href="javascript:void(0)">
            <h1 class="black bold">Instructions</h1>
          </a>
        </div>
      </div>
    </div>

    <div class="courseHeaderContainer-turn">
      <div class="courseHeaderText">
        <h1 class="courseHeaderTextSubject">05506221 Mixed Reality</h1>
        <h1 class="courseHeaderTextTime">Friday 09:00 AM - 12:00 PM</h1>
      </div>
    </div>
    <!-- end header -->

    <div class="row justify-content-center">
      <div class="col-lg-11">
        <v-card class="mx-auto margin-box" min-height="600" style="max-width: 1100px;">
          <!-- top section -->
          <div class="d-flex flex-column p-5">
            <!-- assignment -->
            <div class="d-flex">
              <v-avatar size="60">
                <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
              </v-avatar>

              <div class="d-flex flex-column flex-grow-1 px-3">
                <h6 class="C58595b bold">{{ post.teachname }}</h6>
                <h7>{{ post.date }}</h7>
              </div>

              <h8 class="C58595b">{{ post.point }}&nbsp;&nbsp;Points</h8>
            </div>
            <!-- end assignment -->

            <div class="d-flex mt-5">
              <img src="@/assets/assignment.svg" />
              <div class="d-flex flex-column px-3">
                <h8 class="C58595b bold">{{ post.assign }}</h8>
                <h8 class="pt-3">Due {{ post.date }}</h8>
              </div>
            </div>
          </div>
          <!-- end top -->

          <hr style="border: 1px solid #f8941e" />

          <h8 class="C58595b bold px-5" style="padding-top: 30px;">Class comment</h8>

          <div class="d-flex px-5 py-3">
            <v-avatar size="60">
              <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
            </v-avatar>

            <form class="flex-grow-1">
              <div class="form-group pl-3 d-flex flex-wrap mb-0">
                <v-text-field
                  class="flex-grow-1 pr-3"
                  name="comment"
                  placeholder="Add comment class"
                  color="#000"
                ></v-text-field>
                <v-btn depressed large color="#f8941e">
                  <a style="color: #FFFFFF;">+ Your Work</a>
                </v-btn>
              </div>

              <v-file-input
                :multiple="true"
                v-show="false"
                id="upload-image"
                @change="selectImages($event)"
              ></v-file-input>

              <div class="image-preview">
                <div class="image" v-for="image in images" :key="image.key">
                  <a
                    :href="image.url"
                    target="_blank"
                    class="preview"
                    :style="{backgroundImage: `url(${image.url})`}"
                  ></a>
                  <div class="description">
                    <div class="mb-0 name" :title="image.name">{{ image.name }}</div>
                    <p class="mb-0">{{ image.size }}</p>
                  </div>
                  <div class="control">
                    <v-btn icon small @click="removeImage(image.key)">
                      <v-icon>mdi-close</v-icon>
                    </v-btn>
                  </div>
                </div>
              </div>
              <!-- image-preview -->

              <div class="pt-3">
                <v-btn large color="teal" icon>
                  <v-icon>mdi-paperclip</v-icon>
                </v-btn>
                <v-label large color="teal" icon for="upload-image">
                  <v-icon>mdi-image</v-icon>
                </v-label>
                <v-btn large color="teal" icon>
                  <v-icon>mdi-link</v-icon>
                </v-btn>
              </div>
            </form>
          </div>
          <!-- flex -->
        </v-card>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  background-color: #e5e5e5;
  min-height: calc(1400px);
  width: 100%;
}

.wrapper-tap {
  position: relative;
  display: inline-block;
  background-color: #ffffff;
  width: 100%;
  height: 112px;
}

.html,
.body {
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
  display: block;
  width: 100%;
  background-image: url(~assets/CourseHeader.png);
  background-size: 100% 100%;
  background-repeat: no-repeat;
  min-height: 247px;
}

.margin-box {
  margin-top: 80px;
}

.image-preview {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.image-preview .image {
  display: flex;
  flex-direction: row;
  background-color: white;
  border-radius: 10px;
  padding: 10px;
  border: 1px solid rgb(218, 218, 218);
  margin-right: 5px;
  margin-top: 5px;
  max-width: 250px;
}

.image-preview .image:last-child {
  margin-right: 0;
}

.image-preview .image .preview {
  width: 60px;
  height: 60px;
  min-width: 60px;
  min-height: 60px;
  background-size: cover;
  border-radius: 10px;
}

.image-preview .image .description {
  display: flex;
  flex-direction: column;
  padding-left: 5px;
  overflow: hidden;
  flex-grow: 1;
}

.image-preview .image .description .name {
  display: block;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  font-weight: bold;
}

.image-preview .image .control {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-width: 50px;
}
</style>

<script>
class Post {
  constructor(teachname, stuname, subject, date, point, assign) {
    this.teachname = teachname;
    this.stuname = stuname;
    this.subject = subject;
    this.date = date;
    this.point = point;
    this.assign = assign;
  }
}
import "@/css/font.css";
export default {
  css: "font",
  data() {
    return {
      post: new Post(
        "Witchaya Towongpaichayont",
        "Piyawat Sawong",
        "Mixed Reality",
        "May 4, 2019 (Edited May 11, 2019)",
        "15",
        "New assignment : Quest 030 : AR in your Area (2)"
      ),
      search: "",

      images: []
    };
  },
  computed: {
    filteredList() {
      return this.postList.filter(post => {
        return post.title.toLowerCase().includes(this.search.toLowerCase());
      });
    }
  },

  methods: {
    selectImages(event) {
      if (this.images.legnth > 0) {
        this.images.forEach((image, index) => {
          URL.revokeObjectURL(image.url);
        });
      }
      this.images = [];

      event.forEach((file, index) => {
        this.images.push({
          key: index,
          url: URL.createObjectURL(file),
          name: file.name,
          size: (file.size / Math.pow(1024, 2)).toFixed(2) + " MB"
        });
      });
    },

    removeImage(key) {
      this.images.every((image, index) => {
        if (image.key == key) {
          this.images.splice(index, 1);
          return false;
        }
        return true;
      });
    }
  }
};
</script>
