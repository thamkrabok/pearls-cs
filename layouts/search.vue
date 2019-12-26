<template>
  <div>
    <body class="body">
      <div id="app">
        <div class="search-wrapper">
          <h1 class="course-categories bold C58595b">Course Categories</h1>
          <h2 class="search-course bold C58595b">Search Course</h2>
          <input type="text" v-model="search" placeholder="Search Course"/>
        </div>
        <hr width="100%">
        <div class="wrapper">
          <div class="card" v-for="post in filteredList">
            <a target="_blank">
              <img v-bind:src="post.img"/>
              <h3 class="bold Cf8941e">{{ post.title }}</h3>
              <h10 class="text-center bold detail C58595b">posted by : {{post.author}}</h10>
              <a v-bind:href="post.link">
              <v-btn small color="#f8941e"><h6 class="text-center center-btn bold white">Get Access</h6></v-btn>
              </a>
            </a>
          </div>
        </div>
      </div>
    </body>
  </div>
</template>

<style scoped>
.html, .body {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  margin-top: 16px;
  margin-bottom: 16px;
}

#app {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.center-btn {
  position: relative;
  top: 5px;
}

.course-categories{
  position: relative;
  left: -150%;
  top: 20px;
}

.search-course {
  position: relative;
  left: -150%;
  top: 45px;
}


.search-wrapper {
    position: relative;
    label {
      position: absolute;
      font-size: 12px;
      color: rgba(0,0,0,.50);
      top: 8px;
      left: 12px;
      z-index: -1;
      transition: .15s all ease-in-out;
    }
}

.detail {
  width: 230px;
  max-height: 100px;
}

input {
  padding: 4px 12px;
  color: rgba(0,0,0,.70);
  border: 1px solid rgba(0,0,0,.12);
  transition: .15s all ease-in-out;
  background: white;
  border-radius: 10px;
  width: 300px;
  height: 50px;
  &:focus {
    outline: none;
    transform: scale(1.05);
    & + label  {
      font-size: 10px;
      transform: translateY(-24px) translateX(-12px);
    }
  }
  &::-webkit-input-placeholder {
      font-size: 12px;
      color: rgba(0,0,0,.50);
      font-weight: 100;
    }
}

.wrapper {
   display: flex;
   max-width: 1300px;
   flex-wrap: wrap;
   padding-top: 12px;
 }


 .card {
    box-shadow: rgba(0, 0, 0, 0.117647) 0px 1px 6px, rgba(0, 0, 0, 0.117647) 0px 1px 4px;
    width: 360px;
    margin: 36px;
    max-height: 500px;
    transition: .15s all ease-in-out;
    :hover {
      transform: scale(1.1);
    }
  }


@media only screen and (max-width: 1299px){
  .card {
     box-shadow: rgba(0, 0, 0, 0.117647) 0px 1px 6px, rgba(0, 0, 0, 0.117647) 0px 1px 4px;
     width: 360px;
     margin: 24px;
     max-height: 500px;
     transition: .15s all ease-in-out;
     &:hover {
       transform: scale(1.1);
     }
   }
}

  a {
    text-decoration: none;
    padding: 12px;
    color: #03A9F4;
    font-size: 24px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  img {
    height: 100px;
  }
  small {
    font-size: 10px;
    padding: 4px;
  }

  @media only screen and (min-width: 320px) and (max-width: 419px){
    #app {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      max-width: 300px;
    }

    hr {
      position: relative;
      left:5%;
    }

    .course-categories {
      left: 15%;
      top: 0px;
    }

    .wrapper{
      display: flex;
      max-width: 260px;
      flex-wrap: wrap;
      padding-top: 12px;
    }

    .card {
       box-shadow: rgba(0, 0, 0, 0.117647) 0px 1px 6px, rgba(0, 0, 0, 0.117647) 0px 1px 4px;
       width: 360px;
       margin: 24px;
       left: 5%;
       max-height: 500px;
       transition: .15s all ease-in-out;
       &:hover {
         transform: scale(1.1);
       }
     }

     input {
       position: relative;
       padding: 4px 12px;
       color: rgba(0,0,0,.70);
       border: 1px solid rgba(0,0,0,.12);
       transition: .15s all ease-in-out;
       background: white;
       border-radius: 10px;
       width: 300px;
       height: 50px;
       left: 5%;
       &:focus {
         outline: none;
         transform: scale(1.05);
         & + label  {
           font-size: 10px;
           transform: translateY(-24px) translateX(-12px);
         }
       }
       &::-webkit-input-placeholder {
           font-size: 12px;
           color: rgba(0,0,0,.50);
           font-weight: 100;
         }
     }

     .search-course {
       position: relative;
       left: 25%;
       top: 0px;
     }
  }

  @media only screen and (min-width: 420px) and (max-width: 767px){
    .course-categories {
      left: 30%;
      top: 0px;
    }

    .wrapper{
      display: flex;
      max-width: 260px;
      flex-wrap: wrap;
      padding-top: 12px;
    }

    .card {
       box-shadow: rgba(0, 0, 0, 0.117647) 0px 1px 6px, rgba(0, 0, 0, 0.117647) 0px 1px 4px;
       width: 360px;
       margin: 24px;
       left: 5%;
       max-height: 500px;
       transition: .15s all ease-in-out;
       &:hover {
         transform: scale(1.1);
       }
     }

     .search-course {
       position: relative;
       left: 25%;
       top: 0px;
     }
  }

  @media only screen and (min-width: 768px) and (max-width: 1023px){
    .course-categories {
      left: 10%;
      top: 0px;
    }

    .wrapper{
      display: flex;
      max-width: 400px;
      flex-wrap: wrap;
      padding-top: 12px;
    }

    .search-course {
      position: relative;
      left: 20%;
      top: 0px;
    }
  }

  @media only screen and (min-width: 1024px) and (max-width: 1200px){
    .course-categories {
      left: 10%;
      top: 0px;
    }

    .wrapper{
      display: flex;
      max-width: 820px;
      flex-wrap: wrap;
      padding-top: 12px;
    }

    .search-course {
      position: relative;
      left: 20%;
      top: 0px;
    }
  }

</style>


<script>
class Post {
  constructor(title, link, author, img) {
    this.title = title;
    this.link = link;
    this.author = author;
    this.img = img;
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
          'Vue.js',
          'https://vuejs.org/',
          'Chris',
          'https://vuejs.org//images/logo.png'
        ),
        ,
      new Post(
        'React.js',
        'https://facebook.github.io/react/',
        'Tim',
        'https://daynin.github.io/clojurescript-presentation/img/react-logo.png'
      ),
      new Post(
        'Angular.js',
        'https://angularjs.org/',
        'Sam',
        'https://angularjs.org/img/ng-logo.png'
      ),
      new Post(
        'Ember.js',
        'http://emberjs.com/',
        'Rachel',
        'http://www.gravatar.com/avatar/0cf15665a9146ba852bf042b0652780a?s=200'
      ),
      new Post(
        'Meteor.js',
        'https://www.meteor.com/',
        'Chris',
        'http://hacktivist.in/introduction-to-nodejs-mongodb-meteor/img/meteor.png'
      ),
      new Post(
        'Aurelia',
        'http://aurelia.io/',
        'Tim',
        'https://cdn.auth0.com/blog/aurelia-logo.png'
      ),
      new Post(
        'Node.js',
        'https://nodejs.org/en/',
        'A. A. Ron',
        'https://code-maven.com/img/node.png'
      ),
      new Post(
        'Pusher',
        'https://pusher.com/',
        'Alex',
        'https://avatars1.githubusercontent.com/u/739550?v=3&s=400'
      ),
      new Post(
        'Feathers.js',
        'http://feathersjs.com/',
        'Chuck',
        'https://cdn.worldvectorlogo.com/logos/feathersjs.svg'
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
