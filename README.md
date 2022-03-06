# vue-todolist

### Vue.js와 localstorage를 이용하여 만든 Todo list입니다.
1. Todo.vue
- Todo.vue(상위 컴포넌트)안에 TodoHeader.vue, TodoInput.vue, TodoList.vue (하위 컴포넌트)가 있습니다.
2. TodoHeader.vue
- msg의 prop을 전달하여 헤더에 나타내기
3. TodoInput.vue
- input박스로 텍스트를 입력하면 addTodo 메소드 실행
- addTodo 메소드는 localstorage에 저장하는 이벤트를 실행.
- 해당 이벤트 상위컴포넌트인 Todo.vue로 emit하기
- clearbox메소드 실행 => input박스에 입력된 테스트 초기화.
4. TodoList.vue
- 리스트들이 나타나는 곳 => v-for를 이용하여 나타내기
- 
- 

### Project setup
```
npm install
```
