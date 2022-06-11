<script setup lang="ts">

import ThreadList from "@/components/ThreadList.vue";


</script>

<template>
  <main>
    <div class="container">
      <h1>Welcome to the Forum</h1>

      <ThreadList />
      <!-- <div
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
      </div> -->
    </div>
  </main>
</template>


<style scoped>
</style>