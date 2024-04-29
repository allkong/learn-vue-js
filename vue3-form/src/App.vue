<template>
  <!-- prevent: from의 기본적인 동작을 여기서 막아줄 수 있다 -->
  <form action="" @submit.prevent="submitForm">
    <div>
      <label for="userId">ID:</label>
      <input id="userId" type="text" v-model="username">
    </div>
    <div>
      <label for="password">PW:</label>
      <input id="password" type="text" v-model="password">
    </div>
    <button type="submit">로그인</button>
  </form>
</template>

<script>
  import axios from 'axios'
  import { ref } from 'vue';

  export default {
    // Composition API 방식
    setup() {
      // data
      const username = ref('')
      const password = ref('')

      // methods
      const submitForm = () => {
        axios.post('https://jsonplaceholder.typicode.com/users', {
          username: username.value,
          password: password.value
        }).then(response => {
          console.log(response)
        })
      }

      return {
        username,
        password,
        submitForm
      }
    }

    // Option API 방식
    // data() {
    //   return {
    //     username: '',
    //     password: ''
    //   }
    // },
    // methods: {
    //   submitForm() {
    //     // 폼의 기본적인 동작(새로고침)을 막는다
    //     // event.preventDefault()
    //     const userData = {
    //       username: this.username,
    //       password: this.password
    //     }

    //     axios.post('https://jsonplaceholder.typicode.com/users', userData)
    //       .then(response => {
    //         console.log(response)
    //       })
    //   }
    // }
  }
</script>

<style scoped>

</style>