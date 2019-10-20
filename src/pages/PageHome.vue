<template>
  <div class="col-full">
    <h1>Welcome to the Forum</h1>
    <ThreadList :threads="threads" />
    <ForumList :forums="forums" />
  </div>
</template>

<script>
import sourceData from "@/data";
import ThreadList from "@/components/ThreadList";
import ForumList from "@/components/ForumList";

export default {
  components: {
    ThreadList,
    ForumList
  },

  data() {
    return {
      threads: Object.values(sourceData.threads),
      forums: Object.values(sourceData.forums),
      posts: sourceData.posts,
      users: sourceData.users
    };
  }
};
</script>
