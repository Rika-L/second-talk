---
layout: end
highlighter: shiki
css: unocss
colorSchema: dark
transition: fade-out
mdc: true
glowSize: 0.1
glowX: -100
glowY: 50
---

<div aria-label="Orange and tan hamster running in a metal wheel" role="img" class="wheel-and-hamster">
	<div class="wheel"></div>
	<div class="hamster">
		<div class="hamster__body">
			<div class="hamster__head">
				<div class="hamster__ear"></div>
				<div class="hamster__eye"></div>
				<div class="hamster__nose"></div>
			</div>
			<div class="hamster__limb hamster__limb--fr"></div>
			<div class="hamster__limb hamster__limb--fl"></div>
			<div class="hamster__limb hamster__limb--br"></div>
			<div class="hamster__limb hamster__limb--bl"></div>
			<div class="hamster__tail"></div>
		</div>
	</div>
	<div class="spoke"></div>
</div>

<style>
  .wheel-and-hamster {
  --dur: 1s;
  position: relative;
  width: 12em;
  height: 12em;
  font-size: 14px;
}

.wheel,
.hamster,
.hamster div,
.spoke {
  position: absolute;
}

.wheel,
.spoke {
  border-radius: 50%;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.wheel {
  background: radial-gradient(100% 100% at center,hsla(0,0%,60%,0) 47.8%,hsl(0,0%,60%) 48%);
  z-index: 2;
}

.hamster {
  animation: hamster var(--dur) ease-in-out infinite;
  top: 50%;
  left: calc(50% - 3.5em);
  width: 7em;
  height: 3.75em;
  transform: rotate(4deg) translate(-0.8em,1.85em);
  transform-origin: 50% 0;
  z-index: 1;
}

.hamster__head {
  animation: hamsterHead var(--dur) ease-in-out infinite;
  background: hsl(30,90%,55%);
  border-radius: 70% 30% 0 100% / 40% 25% 25% 60%;
  box-shadow: 0 -0.25em 0 hsl(30,90%,80%) inset,
		0.75em -1.55em 0 hsl(30,90%,90%) inset;
  top: 0;
  left: -2em;
  width: 2.75em;
  height: 2.5em;
  transform-origin: 100% 50%;
}

.hamster__ear {
  animation: hamsterEar var(--dur) ease-in-out infinite;
  background: hsl(0,90%,85%);
  border-radius: 50%;
  box-shadow: -0.25em 0 hsl(30,90%,55%) inset;
  top: -0.25em;
  right: -0.25em;
  width: 0.75em;
  height: 0.75em;
  transform-origin: 50% 75%;
}

.hamster__eye {
  animation: hamsterEye var(--dur) linear infinite;
  background-color: hsl(0,0%,0%);
  border-radius: 50%;
  top: 0.375em;
  left: 1.25em;
  width: 0.5em;
  height: 0.5em;
}

.hamster__nose {
  background: hsl(0,90%,75%);
  border-radius: 35% 65% 85% 15% / 70% 50% 50% 30%;
  top: 0.75em;
  left: 0;
  width: 0.2em;
  height: 0.25em;
}

.hamster__body {
  animation: hamsterBody var(--dur) ease-in-out infinite;
  background: hsl(30,90%,90%);
  border-radius: 50% 30% 50% 30% / 15% 60% 40% 40%;
  box-shadow: 0.1em 0.75em 0 hsl(30,90%,55%) inset,
		0.15em -0.5em 0 hsl(30,90%,80%) inset;
  top: 0.25em;
  left: 2em;
  width: 4.5em;
  height: 3em;
  transform-origin: 17% 50%;
  transform-style: preserve-3d;
}

.hamster__limb--fr,
.hamster__limb--fl {
  clip-path: polygon(0 0,100% 0,70% 80%,60% 100%,0% 100%,40% 80%);
  top: 2em;
  left: 0.5em;
  width: 1em;
  height: 1.5em;
  transform-origin: 50% 0;
}

.hamster__limb--fr {
  animation: hamsterFRLimb var(--dur) linear infinite;
  background: linear-gradient(hsl(30,90%,80%) 80%,hsl(0,90%,75%) 80%);
  transform: rotate(15deg) translateZ(-1px);
}

.hamster__limb--fl {
  animation: hamsterFLLimb var(--dur) linear infinite;
  background: linear-gradient(hsl(30,90%,90%) 80%,hsl(0,90%,85%) 80%);
  transform: rotate(15deg);
}

.hamster__limb--br,
.hamster__limb--bl {
  border-radius: 0.75em 0.75em 0 0;
  clip-path: polygon(0 0,100% 0,100% 30%,70% 90%,70% 100%,30% 100%,40% 90%,0% 30%);
  top: 1em;
  left: 2.8em;
  width: 1.5em;
  height: 2.5em;
  transform-origin: 50% 30%;
}

.hamster__limb--br {
  animation: hamsterBRLimb var(--dur) linear infinite;
  background: linear-gradient(hsl(30,90%,80%) 90%,hsl(0,90%,75%) 90%);
  transform: rotate(-25deg) translateZ(-1px);
}

.hamster__limb--bl {
  animation: hamsterBLLimb var(--dur) linear infinite;
  background: linear-gradient(hsl(30,90%,90%) 90%,hsl(0,90%,85%) 90%);
  transform: rotate(-25deg);
}

.hamster__tail {
  animation: hamsterTail var(--dur) linear infinite;
  background: hsl(0,90%,85%);
  border-radius: 0.25em 50% 50% 0.25em;
  box-shadow: 0 -0.2em 0 hsl(0,90%,75%) inset;
  top: 1.5em;
  right: -0.5em;
  width: 1em;
  height: 0.5em;
  transform: rotate(30deg) translateZ(-1px);
  transform-origin: 0.25em 0.25em;
}

.spoke {
  animation: spoke var(--dur) linear infinite;
  background: radial-gradient(100% 100% at center,hsl(0,0%,60%) 4.8%,hsla(0,0%,60%,0) 5%),
		linear-gradient(hsla(0,0%,55%,0) 46.9%,hsl(0,0%,65%) 47% 52.9%,hsla(0,0%,65%,0) 53%) 50% 50% / 99% 99% no-repeat;
}

/* Animations */
@keyframes hamster {
  from, to {
    transform: rotate(4deg) translate(-0.8em,1.85em);
  }

  50% {
    transform: rotate(0) translate(-0.8em,1.85em);
  }
}

@keyframes hamsterHead {
  from, 25%, 50%, 75%, to {
    transform: rotate(0);
  }

  12.5%, 37.5%, 62.5%, 87.5% {
    transform: rotate(8deg);
  }
}

@keyframes hamsterEye {
  from, 90%, to {
    transform: scaleY(1);
  }

  95% {
    transform: scaleY(0);
  }
}

@keyframes hamsterEar {
  from, 25%, 50%, 75%, to {
    transform: rotate(0);
  }

  12.5%, 37.5%, 62.5%, 87.5% {
    transform: rotate(12deg);
  }
}

@keyframes hamsterBody {
  from, 25%, 50%, 75%, to {
    transform: rotate(0);
  }

  12.5%, 37.5%, 62.5%, 87.5% {
    transform: rotate(-2deg);
  }
}

@keyframes hamsterFRLimb {
  from, 25%, 50%, 75%, to {
    transform: rotate(50deg) translateZ(-1px);
  }

  12.5%, 37.5%, 62.5%, 87.5% {
    transform: rotate(-30deg) translateZ(-1px);
  }
}

@keyframes hamsterFLLimb {
  from, 25%, 50%, 75%, to {
    transform: rotate(-30deg);
  }

  12.5%, 37.5%, 62.5%, 87.5% {
    transform: rotate(50deg);
  }
}

@keyframes hamsterBRLimb {
  from, 25%, 50%, 75%, to {
    transform: rotate(-60deg) translateZ(-1px);
  }

  12.5%, 37.5%, 62.5%, 87.5% {
    transform: rotate(20deg) translateZ(-1px);
  }
}

@keyframes hamsterBLLimb {
  from, 25%, 50%, 75%, to {
    transform: rotate(20deg);
  }

  12.5%, 37.5%, 62.5%, 87.5% {
    transform: rotate(-60deg);
  }
}

@keyframes hamsterTail {
  from, 25%, 50%, 75%, to {
    transform: rotate(30deg) translateZ(-1px);
  }

  12.5%, 37.5%, 62.5%, 87.5% {
    transform: rotate(10deg) translateZ(-1px);
  }
}

@keyframes spoke {
  from {
    transform: rotate(0);
  }

  to {
    transform: rotate(-1turn);
  }
}
</style>

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
glowX: 80
glowY: 80
layout: intro
---

<h3 class="op50"> Back End </h3>

## 后端代码规范

---
glowX: 50
glowY: 50
layout: center
---

<h3 class="font-thin">0 === [否] false</h3>

<h3 class="font-thin">1 === [是] true</h3>

---
glowX: 80
glowY: 50
---

## 二、命名规范
<v-clicks>
### 数据库命名
使用下划线命名
```
user_id
```

### 代码里
使用驼峰命名
```
userId
```

### 接口路径
使用斜线分隔的命名
```
user/list
```

</v-clicks>

---
glowX: 50
glowY: 70
layout: center
---

# 三、数据库规范

---
glowX: 50
glowY: 10
layout: center
---

##### （1）命名规范

- 建库时每个表每个字段都应写好注释。每个字段的主键应使用表名加id，比如用户表主键应为：user_id。

---
glowX: 20
glowY: 30
layout: center
---


##### （2）设计规范

- 使用第三范式设计数据库，比如有一个表为menu表，它记录了所有的菜单对应权限，而一个用户可能有多个权限担任，如果将menu_id绑定在user表，那么就可能一个用户有多个列，造成数据冗余。所以应创一个新表，单独记录user与menu的关系。这也相当于一种外键，只不过不是直接在数据库建立外键，而是在代码里进行逻辑上的外键绑定。前者称为物理外键，现在很多大公司都是不允许使用的。

<img src="/2.png" width="400">

---
glowX: 40
glowY: 40
layout: center
---

##### （3）结构规范

- 存储重要信息的表都应有以下四个字段（如果非常重要或者公司有要求可能还有更多）：create_id、create_time、update_id、update_time，记录该条数据的操作者及修改时间。并且应有一个日志表来记录这些操作。

<img src="/3.png" width="400">

---
glowX: 50
glowY: 90
layout: center
---

## 四、代码规范

---
glowX: 60
glowY: 60
layout: center
---

##### （1）代码结构

- 代码应按照功能进行建包，并把相应的类放在对应的包下。比如有若干类执行定时任务，则建一个task包，把所有相关的类放到该包下。

<img src="/4.png" width="700">

---
glowX: 60
glowY: 90
layout: center
---

##### （2）类的命名

- 类的命名应见名知意，实体类的命名应按照规范：直接对应数据库的用entity作为后缀，如userEntity，用于接收前端传参的用DTO作为后缀，用于存储数据库查询结果或作为回传前端的实体类后缀应使用VO。


---
glowX: 50
glowY: 90
layout: center
---

##### （3）复用思想


- 有可以复用的方法应专门建个类进行存放，如从数据库获取token。

```java
public class UserRequestUtils {
    /**
     * 获取请求头中的token工具类
     */
    public static String getCurrentToken() {
        HttpServletRequest request = ((ServletRequestAttributes) Objects.requireNonNull(RequestContextHolder.getRequestAttributes()))
                .getRequest();
        return request.getHeader("token");
    }
}
```




---
glowX: 50
glowY: 90
layout: center
---

##### （4）参数配置

- 尽量配置在配置文件yml中，进行统一管理。

<img src="/5.png" width="400">

---
glowX: 10
glowY: 10
layout: center
---

##### （5）项目日志

- 区别于数据库日志是记录操作的，项目日志是为了方便维护的，便于报错时直接定位到是哪个方法出现了问题。

```java
log.info("用户注册")
```

---
glowX: 50
glowY: 10
layout: center
---

##### （6）数据校验

- 有时候前端传来的数据是非法的，如学号是10位，实际传的却不是，有可能是用户填写错误，这时应进行校验，如是非法数据应返回提示给用户。

<img src="/6.png" width="600">

---
glowX: 50
glowY: 90
layout: center
---

##### （7）异常处理

- 在可能导致报错的地方应使用try catch包围，并做好异常的记录，方便后续维护。

```java {2,8-10}{lines:true}
public static String generateValue(String param) {
    try {
        MessageDigest algorithm = MessageDigest.getInstance("MD5");
        algorithm.reset();
        algorithm.update(param.getBytes());
        byte[] messageDigest = algorithm.digest();
        return toHexString(messageDigest);
    } catch (Exception e) {
        throw new RRException("生成Token失败", e);
    }
}
```

---
glowX: 10
glowY: 10
glowSize: 0.9
layout: center
---

<h1 class="op50 font-thin">  提交规范 </h1>

---
layout: center
---

```
'feat',//新功能（feature）
'fix',//修改bug
'perf',//表示该提交用于提高性能
'style',//代码格式修改, 注意不是 css 修改(不影响代码运行的变动)
'docs',//文档修改（documentation）
'test',//表示该提交用于测试代码
'refactor',//代码重构
'build',//编译相关的修改，例如发布版本、对项目构建或者依赖的改动
'ci',//持续集成
'chore',//其他修改, 比如改变构建流程、或者增加依赖库、工具等
'revert',//回滚到上一个版本
'wip',//大改动但未完成，方便知道你还在work
```

---
glowX: 10
glowY: 90
glowSize: 0.9
---
### front-end: practicing

<div class="flex gap-2">
<img src="/7.png" width="200">
<img src="/8.png" width="200">
<img src="/9.png" width="200">
<img src="/10.png" width="200">
</div>


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

<img src="/exam.jpg" width="400">

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

<div class="font-thin text-9xl">
  The End
</div>

<div class="loader"></div>

<style>
  .loader {
  position: relative;
  width: 120px;
  height: 90px;
  margin: 0 auto;
}

.loader:before {
  content: "";
  position: absolute;
  bottom: 30px;
  left: 50px;
  height: 30px;
  width: 30px;
  border-radius: 50%;
  background: #2a9d8f;
  animation: loading-bounce 0.5s ease-in-out infinite alternate;
}

.loader:after {
  content: "";
  position: absolute;
  right: 0;
  top: 0;
  height: 7px;
  width: 45px;
  border-radius: 4px;
  box-shadow: 0 5px 0 #f2f2f2, -35px 50px 0 #f2f2f2, -70px 95px 0 #f2f2f2;
  animation: loading-step 1s ease-in-out infinite;
}

@keyframes loading-bounce {
  0% {
    transform: scale(1, 0.7);
  }

  40% {
    transform: scale(0.8, 1.2);
  }

  60% {
    transform: scale(1, 1);
  }

  100% {
    bottom: 140px;
  }
}

@keyframes loading-step {
  0% {
    box-shadow: 0 10px 0 rgba(0, 0, 0, 0),
            0 10px 0 #f2f2f2,
            -35px 50px 0 #f2f2f2,
            -70px 90px 0 #f2f2f2;
  }

  100% {
    box-shadow: 0 10px 0 #f2f2f2,
            -35px 50px 0 #f2f2f2,
            -70px 90px 0 #f2f2f2,
            -70px 90px 0 rgba(0, 0, 0, 0);
  }
}
</style>
