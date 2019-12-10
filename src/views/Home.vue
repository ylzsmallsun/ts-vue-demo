<template>
  <div class="home">
    <h1 class="pageTitle">Typescript demo page</h1>
    <BlogPost v-for="blog in blogPosts" :post="blog" :key="blog.title"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue} from 'vue-property-decorator';
// @ is an alias to /src
import BlogPost, { IPost } from '@/components/BlogPost.vue';

@Component({
  components: {
    BlogPost
  }
})

export default class Home extends Vue {
  private blogPosts: IPost[] = [
    {
      title: 'My first blogpost ever!',
      subTitle: 'Lorem ipsum dolor sit amet.',
      author: 'Mike',
      datePosted: new Date(2018, 12, 10)
    },
    {
      title: 'Look I am blogging!',
      subTitle: 'Hurray for me, this is my second post.',
      author: 'Mike',
      datePosted: new Date(2019, 1, 16)
    },
    {
      title: 'You don\'t known javascript!',
      subTitle: 'Something you need to know.',
      author: 'Mike',
      datePosted: new Date(2019, 11, 22)
    },
  ];

  private mounted(): void {
    // console.log(this.blogPosts);
  }
}

</script>
<style scoped>
.pageTitle {
  color: orangered;
}
</style>
