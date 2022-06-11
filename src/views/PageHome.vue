<script setup lang="ts">
import SourceData from "@/datasource/datasource";

const threads = SourceData.threads;
const posts = SourceData.posts;
const users = SourceData.users;
console.log(threads)
function getPostById(id) {
  return posts.find((p) => p.id === id);
}

function getUserById(id: string) {
  return users.find((u) => u.id === id);
}
</script>

<template>
  <main>
    <div class="container">
      <div
        class="col-large push-top"
        v-for="thread in threads"
        :key="thread.id"
      >
        <h1>{{ thread.title }}</h1>

        <div class="post-list">
          <div v-for="postId in thread.posts" :key="postId" class="post">
            <div class="user-info">
              <a href="#" class="user-name">{{
                getUserById(getPostById(postId).userId).name
              }}</a>

              <a href="#">
                <img
                  class="avatar-large"
                  :src="getUserById(getPostById(postId).userId).avatar"
                  alt=""
                />
              </a>

              <p class="desktop-only text-small">107 posts</p>
            </div>

            <div class="post-content">
              <div>
                <p>
                  {{ getPostById(postId).text }}
                </p>
              </div>
            </div>

            <div class="post-date text-faded">
              {{ getPostById(postId).publishedAt }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>


<style scoped>


</style>