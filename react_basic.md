
# 一些react的基础笔记

## 体验一下react

```js
			ReactDOM.render(<h1>Hello React</h1>, document.getElementById('root'));
```

## JSX小分队

```js
			const ele = <h1>test ele</h1>
			ReactDOM.render(ele, document.getElementById('root'))
```

在jsx中嵌入表达式

```js
			const name = 'demo'
			const ele = <h1>{name}</h1>
			ReactDOM.render(ele, document.getElementById('root'))
```

调用函数渲染到页面中

```js
			function getName(user) {
				return user.firstName
			}
			const user = {
				firstName: 'Tom'
			}
			const ele = <h1>{getName(user)}</h1>
			ReactDOM.render(ele, document.getElementById('root'))
```

JSX 也是一个表达式

```js
			function getGreeting(user) {
				if (user) {
					return <h1>{getName(user)}</h1>
				}
				return <h1>dddd</h1>
			}
			function getName(user) {
				return user.firstName
			}
			const user = {
				firstName: 'Tom'
			}
```

属性中嵌入表达式的时候 不要在大括号外面加上引号

只有属性值为字符串字面量的时候才使用引号

不要同个属性同时使用两种符号

```js
			const ele = <div index="0"></div>
			const img = <img src={user.url}></img>
```

jsx使用小驼峰命名法

class为className tabindex为tabIndex

JSX 表示对象

```js
			const ele = (
				<h1 className="greeting">
					test
				</h1>
			)
			// 上面的代码 babel会将jsx转译为React.createElement()函数调用
			const ele = React.createElement(
				'h1',
				{className="greeting"},
				'test'
			)
			// React.createElement()实际会创建这样一个对象
			const ele = {
				type: 'h1',
				props: {
					className="greeting",
					chilren: 'test'
				}
			}
```













































------
![end](https://gitee.com/techpang/img_emoji_libs/raw/master/img_bed/markdown_images/end.jpg '富婆加我吧不想努力了')
