<template >
    <div class="col-full">
        <div class="thread">
            <h2 class="list-title">liste of threads</h2>
            <div v-for="thread in threads" :key="thread.id" class="thread">
                <div>
                    <p><a href="#">{{ thread.title }}</a></p>
                    <p class="text-fade text-xsmall">
                        by <a href="">{{getUserById(thread.userId)?.username}}</a>, {{thread.publishedAt}}
                    </p>
                </div>
            </div>
        </div>

    </div>
</template>


<script setup lang="ts">
import SourceData from "@/datasource/datasource";


const threads = SourceData.threads;
const posts = SourceData.posts;
const users = SourceData.users;
console.log(threads)
function getPostById(id: string) {
    return posts.find((p) => p.id === id);
}

function getUserById(id: string) {
    return users.find((u) => u.id === id);
}
</script>
<style lang="">
    
</style>