<template>
  <div class="social-media-post">
    <div class="user-profile">
      <slot name="profile"></slot>
    </div>
    <div class="post-body">
      <slot></slot>
    </div>
    <div class="comments">
      <slot
        name="comments"
        v-for="(comment, i) in comments"
        :key="i"
        :commentText="comment"
      ></slot>
    </div>
  </div>
</template>
  
  <script>
export default {
  name: "SocialMediaPost",
  props: {
    comments: Array, // Assume comments are passed as a prop
  },
};
</script>
  
  <style scoped>
/* Add styles for the social media post component */
.social-media-post {
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 20px;
  margin-bottom: 20px;
}

.user-profile {
  margin-bottom: 10px;
}

.user-profile img {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-right: 10px;
}

.user-profile h3 {
  margin: 0;
}

.post-body {
  margin-bottom: 10px;
}

.comments {
  border-top: 1px solid #ccc;
  padding-top: 10px;
}

.comments h4 {
  margin-top: 0;
}
</style>
  