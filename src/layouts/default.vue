<template>
  <Wrap :page="page">
    <div class="home">
      <h1 class="page-heading" v-if="page.title">{{ page.title }}</h1>

      <slot name="default"></slot>

      <h2
        class="post-list-heading"
        v-if="page.posts && page.posts.length > 0"
      >{{ page.listTitle || "Posts" }}</h2>

      <ul class="post-list" v-if="page.posts && page.posts.length > 0">
        <li v-for="post in page.posts" :key="post.permalink">
          <h3>
            <saber-link class="post-link" :to="post.permalink">
              {{
              post.title
              }}
            </saber-link>
          </h3>
          <span class="post-meta-list">Posted on {{ formatDate(post.createdAt) }}</span>
          <span v-html="post.excerpt" class="post-section"></span>
          <div class="post-read-more-section">
            <a :href="post.permalink" class="post-read-more">Read More</a>
          </div>
        </li>
      </ul>

      <div
        class="pagination"
        v-if="
          page.pagination &&
            (page.pagination.hasNext || page.pagination.hasPrev)
        "
      >
        <router-link
          class="prev-link"
          :to="page.pagination.prevLink"
          v-if="page.pagination.hasPrev"
        >← Previous</router-link>
        <router-link
          class="next-link"
          :to="page.pagination.nextLink"
          v-if="page.pagination.hasNext"
        >Next →</router-link>
      </div>

      <!-- <p class="feed-subscribe" v-if="feedLink">
        <svg class="svg-icon grey">
          <use :xlink:href="getSvg('rss')"></use>
        </svg>
        <a :href="feedLink">Subscribe</a>
      </p>-->
    </div>
  </Wrap>
</template>

<script>
import formatDate from "../utils/formatDate";
import Wrap from "../components/Wrap.vue";
import getSvg from "../utils/getSvg";

export default {
  components: {
    Wrap
  },

  props: ["page"],

  computed: {
    feedLink() {
      return this.$feed && this.$feed.permalink;
    }
  },

  methods: {
    formatDate,
    getSvg
  }
};
</script>
