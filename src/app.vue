<template>
<div class="app">
    <video id="video-demo" class="video-js vjs-default-skin" controls preload="none" webkit-playsinline playsinline data-setup="{}">
    	<source src="https://s3.meituan.net/v1/mss_70cc7da2c5b54ef490d1b5a475e17e3f/edu-video/943747a70fe3e08f04172f5037cd8dcc.mp4" type="video/mp4">
  	</video>
</div>
</template>

<script>
import videoJS from 'video.js/dist/video.min.js'
import 'video.js/dist/video-js.min.css'
export default {
    name: 'app',
    components: {
    },
    mounted () {
        var player = videoJS('#video-demo',{
            techOrder: ["html5"],
            mydata: {
            }

        },function(){

        });
    
        
        player.on('play',function(e){
            console.log('play')
        });
    }
}
</script>

<style scoped lang="less" rel="stylesheet/less">
.app {
    #video-demo{
        width: 100%;
        height: 30%;
    }
}
</style>
