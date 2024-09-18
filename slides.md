---
layout: center
highlighter: shiki
css: unocss
colorSchema: dark
transition: fade-out
mdc: true
glowSize: 0.1
glowX: -100
glowY: 50
---

<LoadingRound/>

---
layout: center
---

<h1 flex="~ col">
<div text-2xl op50>别写"屎山"代码</div>
<div class="font-thin">Code Style Guide</div>
</h1>


<div uppercase text-sm tracking-widest op50>
前端: 李卓熙 | 后端: 林向阳
</div>

---
glowX: 80
glowY: 80
layout: intro
---

<h3 class="op50"> Front End </h3>

## 前端代码规范

---
glowX: 50
glowY: 50
glowSize: 0.5
layout: center
---

<h1 class="font-thin">变量命名</h1>

<v-clicks>

<h2 class="absolute top-25% left-25%"> CamelCase </h2>
<h2 class="absolute top-25% right-25%"> camelCase </h2>
<h2 class="absolute bottom-25% left-25%"> snake_case </h2>
<h2 class="absolute bottom-25% right-25%"> SNAKE_CASE </h2>

</v-clicks>

<style>
h2{
    font-weight: 100;
}
</style>

---
glowX: 80
glowY: 20
layout: intro
---

<h3 class="op50"> Function </h3>

## 函数命名

---
glowX: 10
glowY: 10
glowSize: 0.8
---

# 函数命名

<v-clicks>
<h5> 符合语义的 </h5>
<h5> 最好一眼能看懂 </h5>

<h5> Bad Example </h5>

```ts
function huoquxingming() {
}
```

```ts
function getName() {
}
```



</v-clicks>

<style>
h5{
    font-weight: 100;
    margin-top: 20px;
}
</style>

---
glowX: 80
glowY: 50
layout: intro
---

<h3 class="op50"> 参照vue2风格指南 </h3>

## Vue的一些约束

---
glowX: 10
glowY: 10
glowSize: 0.8
---

# 组件名为多个单词

<v-clicks>
<h5> "组件名应该始终是多个单词的" </h5>
<h5> 这样做可以避免跟现有的以及未来的 HTML 元素相冲突，因为所有的 HTML 元素名称都是单个单词的。 </h5>


<h5> Bad Example </h5>

```vue
<script setup lang="ts">
  defineOptions({
    name:'Todo'
  })
</script>
```

<h5> Good Example </h5>

```vue
<script setup lang="ts">
  defineOptions({
    name:'TodoItem'
  })
</script>
```


</v-clicks>

<style>
h5{
    font-weight: 100;
    margin-top: 20px;
}
</style>

---
glowX: 90
glowY: 10
glowSize: 0.8
---

# Prop 定义

<v-clicks>
<h5> "Prop 定义应该尽量详细" </h5>
<h5> 至少也应该指定类型 </h5>

<h5> Bad Example </h5>

```vue
<script setup lang="ts">
  defineProps(['status'])
</script>
```

<h5> Good Example </h5>

```vue

<script setup lang="ts">
  defineProps<{status:string}>()
</script>
```



</v-clicks>

<style>
h5{
    font-weight: 100;
    margin-top: 20px;
}
</style>

---
glowX: 90
glowY: 90
glowSize: 0.9
---

# 为`v-for`设置键值

<v-clicks>
<h5> "总是用 key 配合 v-for" </h5>


<h5> Bad Example </h5>

```html

<ul>
    <li v-for="todo in todos">
        {{ todo.text }}
    </li>
</ul>
```

<h5> Good Example </h5>

```html
<ul>
  <li
      v-for="todo in todos"
      :key="todo.id"
  >
    {{ todo.text }}
  </li>
</ul>
```

</v-clicks>

<style>
h5{
    font-weight: 100;
    margin-top: 20px;
}
</style>

---
glowX: 90
glowY: 10
glowSize: 0.9
---

# 单组件文件名的大小写（强烈推荐）

<v-clicks>
<h5> 单文件组件的文件名应该要么始终是单词大写开头，要么始终是横线连接。 </h5>

<h5> Bad Example </h5>

```
components/
|- mycomponent.vue

or

components/
|- myComponent.vue
```

<h5> Good Example </h5>

```
components/
|- MyComponent.vue

or

components/
|- my-component.vue
```

</v-clicks>

<style>
h5{
    font-weight: 100;
    margin-top: 20px;
}
</style>

---
glowX: 10
glowY: 10
glowSize: 0.9
layout: intro
---

<h3 class="op50">  Api </h3>

# 接口规范

---
glowX: 50
glowY: 50
glowSize: .5
layout: center
---

# RESTful API

##### 一种设计风格
##### 一种软件架构风格
##### 而不是标准
##### 只是提供了一组设计原则和约束条件

<style>
h5{
    font-weight: 100;
    opacity: 50%;
}
</style>

---
glowX: 10
glowY: 50
glowSize: 1
---

# RESTful 的 六大原则

## 只讲一个：Uniform Interface（统一接口）

<v-clicks>

<div op-50>客户端只需要关注实现接口就可以，接口的可读性加强，使用人员方便调用。</div>

```
GET：获取资源信息。
POST：创建一个新资源。
PUT：更新已有的资源。
DELETE：删除已有的资源。
```

<div op-50>
当 API 数量非常多，系统非常复杂时，RESTful 的好处会越来越明显。理解系统时，可以直接围绕一系列资源来理解和记忆。
</div>

</v-clicks>

---
glowX: 10
glowY: 90
glowSize: 1
layout: center
---

# Example

```
      获取用户   GET     /users   
      新增用户   POST    /users   
      修改用户   PUT     /users/1  
      删除用户   DELETE  /users/1          
```

---
glowX: 50
glowY: 50
glowSize: 1
layout: center
---

<h1 class="font-thin">
  Real Example
</h1>

---
glowX: 20
glowY: 80
glowSize: .6
layout: center
---
# 对前端不太友好的API数据接口

---
glowX: 50
glowY: 50
glowSize: .6
layout: center
---

```json
{
  "code": 200,
  "msg": "success",
  "name": "张三",
  ...各种数据
}
```

---
glowX: 20
glowY: 20
glowSize: .6
layout: center
---

<h1 class="font-thin op-50">Example</h1>

---
glowX: 80
glowY: 80
glowSize: .6
layout: center
---
# 对前端友好的API数据接口

---
glowX: 50
glowY: 50
glowSize: .6
layout: center
---

```json
{
  "code": 200,
  "msg": "success",
  "data": "返回的数据"
}
```

---
glowX: 80
glowY: 20
glowSize: .6
layout: center
---

<h1 class="font-thin op-100">Example</h1>

---
glowX: 50
glowY: 50
glowSize: .5
layout: center
---

<h1 class="font-thin">
  Some Mistake
</h1>

---
glowX: 50
glowY: 0
glowSize: 1
layout: center
---

<img src="/public/exam.jpg" width="400">

---
glowX: 50
glowY: 50
glowSize: .5
layout: center
---

<h1 class="font-thin">
  复现一下
</h1>

---
glowX: 50
glowY: 50
glowSize: .5
layout: end
---

<h1 class="font-thin">
  The End
</h1>

