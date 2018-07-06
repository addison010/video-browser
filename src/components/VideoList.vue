<template>
    <ul class="list-group col-md-4">
        <VideoListItem 
        v-for="(video,index) in videos" 
        :video="video" 
        :key="index" 
        @videoSelect="onVideoSelect">
        </VideoListItem>
    </ul>
</template>

<script>
import VideoListItem from './VideoListItem';

export default {
    name: 'VideoList',
    components: {
        VideoListItem
    },
    props: {
        videos: Array //Prop type validation check
    },
    data() {
        return {
            
        }
    },
    methods: {
        onVideoSelect(video) {
            this.$emit("videoSelect", video)
        }
    }
}
</script>

<style>

</style>
