<template >
    <div class="col-full">
        <div class="thread">
            <h2 class="list-title">liste of threads</h2>
            <div class="flex thread bg-white odd:bg-gray-100 justify-between p-4" v-for="thread in threads" :key="thread.id" >
                <div>
                    <p><a href="#">{{ thread.title }}</a></p>
                    <p class="text-fade text-xsmall">
                        by <a href="">{{getUserById(thread.userId)?.username}}</a>, {{thread.publishedAt}}
                    </p>
                </div>
                <div class="activity">
                    <p class="replies-count">
                            {{thread.posts.length}} replies
                    </p>
                    <img class="avatar-medium" :src="getUserById(thread.userId)?.avatar" alt="">
                </div>    
            </div>
        </div>

    </div>
</template>


<script setup lang="ts">
import SourceData from "@/datasource/datasource";
import {defineProps} from "vue";

const {threads} = defineProps({
    threads:{
        type:Object
    }
})


const posts = SourceData.posts;
const users = SourceData.users;

function getPostById(id: string) {
    return posts.find((p) => p.id === id);
}

function getUserById(id: string) {
    return users.find((u) => u.id === id);
}
</script>
<style lang="">
    
</style>