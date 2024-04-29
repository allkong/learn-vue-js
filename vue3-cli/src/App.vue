<!-- 
  싱글 파일 컴포넌트: 화면의 특정 영역에 대한 HTML, CSS, JS 코드를 한 파일(.vue)에서 관리하는 방법
  https://joshua1988.github.io/vue-camp/vue/sfc.html
 -->

<!-- HTML -->
<template>
  <AppHeader v-bind:appTitle="message" v-on:change="changeMessage"></AppHeader>
</template>

<!-- JavaScript -->
<script>
  // import 라이브러리 from '라이브러리이름'
  // import 파일이름 from './파일경로'
  import AppHeader from './components/AppHeader.vue'

  export default {
    components: {
      // '컴포넌트 이름': 컴포넌트 내용
      // 'AppHeader': AppHeader
      // AppHeader: AppHeader
      AppHeader
    },
    // 인스턴스 옵션 속성
    data() {
      return {
        message: '앱 헤더 컴포넌트'
      }
    },
    methods: {
      changeMessage() {
        this.message = '변경됨'
      }
    }
  }
</script>

<!-- CSS -->
<style scoped>

</style>