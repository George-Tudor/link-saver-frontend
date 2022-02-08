<template>
  <div>
    <h3>{{ header }}</h3>
    <div class="form mb-3">
    <div class="form-group">
        <div class="form-group">
          <label>Link Address: </label>
          <input class="form-control" type="text" v-model="link.url">
        </div>
        <div class="form-group">
          <label>Tags: </label>
          <input class="form-control" type="text" v-model:="link.tags">
        </div>
      </div>
      <button class="btn btn-primary" @click="addLink">Submit</button>
    </div>
    <div class="col-sm-12 row">
      <div class="col-sm-4 link" v-for="(link, index) in links" :key="index">
        <div class="card mb-2">
          <div class="card-block">
            <img :src="link.image" alt="link-image" style="width:100%">
            <h4 class="card-title">{{ link.title }}</h4>
            <h6 class="card-subtitle mb-2 text-muted">{{ link.description }}</h6>
            <p>Tags: </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Links',
  data() {
    return {
      header: 'Link Saver',
      link: {
        title: '',
        description: '',
        image: '',
        url: '',
        tags: [],
      },
        links: [
          {
            index: 0,
            title: 'align-self | CSS-Tricks',
            description: 'The align-self property is a sub-property of the Flexible Box Layout module.',
            image: 'https://css-tricks.com/wp-json/social-image-generator/v1/image/21208',
            url: 'https://css-tricks.com/almanac/properties/a/align-self/',
            tags: []
          },
          {
            index: 1,
            title: 'Bootstrap 4 Tabs - examples & tutorial. Basic & advanced usage - Material Design for Bootstrap',
            description: 'Bootstrap tabs are components which separate content placed in the same wrapper but in the separate pane. Only one pane can be displayed at the time.',
            image: 'https://mdbcdn.b-cdn.net/wp-content/uploads/2016/05/tabs-fb.jpg',
            url: 'https://mdbootstrap.com/docs/b4/jquery/components/tabs/',
            tags: []
          },
          {
            index: 2,
            title: 'Randall Degges - How to Have Fun Programming',
            description: 'Having fun programming is something that a lot of programmers forget how to do -- and that makes me sad. Check this shit out.',
            image: 'https://www.rdegges.com/static/images/favicons/apple-icon-180x180.png',
            url: 'https://www.rdegges.com/2012/how-to-have-fun-programming/',
            tags: []
          },
          {
            index: 3,
            title: '21 Best Healthy Cooking Hacks of All Time | Eat This Not That',
            description: 'If you’re looking to make your cooking healthier and convenient, there are a few healthy cooking hacks you can keep in mind for future culinary adventures.',
            image: 'https://www.eatthis.com/wp-content/uploads/sites/4/2020/08/cooking-shrimp.jpg?fit=1200%2C879&ssl=1',
            url: 'https://www.eatthis.com/best-healthy-cooking-hacks/',
            tags: []
          },
          {
            index: 4,
            title: 'Journey — Learn WebGL with Three.js',
            description: 'The ultimate Three.js course whether you are a beginner or a more advanced developer',
            image: 'https://threejs-journey.com/assets/social/open-graph-image-1200x630.png',
            url: 'https://threejs-journey.xyz/Three.js',
            tags: []
          }
        ]
    }
  },
  methods: {
    addLink() {
      let { url, tags }= this.link;
      this.links.push({
        url,
        tags
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  font-size: 1.75rem;
  margin: 40px 0 0;
  font-weight: 500;
  line-height: 1.2;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.form {
  text-align: left;
}

.card {
  text-align: left;
  border: 1px solid #2c3e50;
  border-radius: 4px;
  padding-top: 8px;
  padding-left: 8px;
  padding-right: 8px;
}
</style>
