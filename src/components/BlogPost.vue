<template>
  <div class="blogList">
    <h2>{{ post.title }}</h2>
		<p>{{ post.subTitle }}</p>
		<p class="meta">Written by {{ post.author }} on {{ date }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

export interface IPost {
  title: string;
  subTitle: string;
  author: string;
  datePosted: Date;
}

@Component
export default class HelloWorld extends Vue {
  @Prop() private post!: IPost;
  get date() {
    return `${ this.post.datePosted.getDate() }/${ this.post.datePosted.getMonth() }/${ this.post.datePosted.getFullYear() }`;
  }

  private mounted(): void {
    console.log('blog: ', this.post);
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2 {
  text-decoration: underline;
}
p.meta {
  font-style: italic;
}
</style>
