# [this](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/this)

## this 指向

| 场景                      | 效果                                                                                                                                                          |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 直接调用                  | 被直接调用时，this 指全局对象 window/global （`严格模式下，this将保持他进入执行环境时的值，this 为 undefined`）                                               |
| bind 方法                 | 调用 f.bind(someObject)会创建一个与 f 具有相同函数体和作用域的函数，但是在这个新函数中，this 将永久地被绑定到了 bind 的第一个参数，无论这个函数是如何被调用的 |
| apply 或 call 方法        | 使用函数的 apply 或 call 方法调用时，this 指第一个参数。                                                                                                      |
| 箭头函数                  | 与声明箭头函数的上下文绑定到一起(箭头函数不会创建自己的 this,它只会从自己的作用域链的上一层继承 this)                                                         |
| 作为对象的方法            | 当函数作为对象里的方法被调用时，它们的 this 是调用该函数的对象                                                                                                |
| 原型链中的 this           | 如果该方法存在于一个对象的原型链上，那么 this 指向的是调用这个方法的对象，就像该方法在对象上一样                                                              |
| 作为构造函数              | 当一个函数用作构造函数时（使用 new 关键字），它的 this 被绑定到正在构造的新对象                                                                               |
| 作为一个 DOM 事件处理函数 | 当函数被用作事件处理函数时，它的 this 指向触发事件的元素                                                                                                      |
| 作为一个内联事件处理函数  | this 指向监听器所在的 DOM 元素                                                                                                                                |
