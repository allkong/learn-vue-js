[Cracking Vue.js - 템플릿 문법](https://joshua1988.github.io/vue-camp/vue/template.html)

<br>

# Vue 템플릿 문법 (Template Syntax)
- 뷰로 화면을 조작하는 방법

## 데이터 바인딩
- [공식 문서](https://vuejs.org/guide/essentials/template-syntax.html#template-syntax)
- 뷰 인스턴스에서 정의한 속성들을 화면에 표시하는 방법
- Mustache Tag(콧수염 괄호) 방식
  ```html
  <div>{{ message }}</div>
  ```
  ```javascript
  Vue.createApp({
    data() {
      return {
        message: 'Hello Vue.js'
      }
    }
  })
  ```

## 디렉티브
- [공식 문서](https://vuejs.org/api/built-in-directives.html#built-in-directives)
- 뷰로 화면의 요소를 더 쉽게 조작하기 위한 문법
  ```html
  <div>
    Hello <span v-if="show">Vue.js</span>
  </div>
   ```
   ```javascript
   Vue.createApp({
   data() {
     return {
       show: false
     }
   }
  })
  ```