<template>
  <div id="app">
    <social-media-post
      v-for="(item, index) in posts"
      :key="index"
      :comments="item.postComments"
    >
      <template v-slot:profile>
        <div class="profile-info">
          <img src="@/assets/user.jpeg" alt="User Avatar" />
          <h3>{{ item.userName }}</h3>
          <p>{{ item.postDate }}</p>
        </div>
      </template>
      <p>{{ item.postContent }}</p>
      <h4>Comments</h4>
      <template v-slot:comments="{ commentText }">
        <li>{{ commentText.text }}</li>
      </template>
    </social-media-post>
  </div>
</template>
  
  <script>
import SocialMediaPost from "./SocialMediaPost.vue";

export default {
  data() {
    return {
      posts: [
        {
          userName: "John Thomas",
          postDate: "April 30, 2024",
          postContent:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          postComments: [
            { id: 1, text: "Great post!" },
            { id: 2, text: "Thanks for sharing." },
          ],
        },
        {
          userName: "Jason Doe",
          postDate: "April 10, 2004",
          postContent:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
          postComments: [
            { id: 1, text: "Awesome!" },
            { id: 2, text: "Good Picture." },
          ],
        },
      ],
    };
  },
  components: {
    SocialMediaPost,
  },
};
</script>
  
  <style>
ul {
  list-style-type: none;
}
.comments-section {
  text-align: center;
}
</style>
  