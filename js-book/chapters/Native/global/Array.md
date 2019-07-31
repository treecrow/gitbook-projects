# [Array](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array)

> JavaScript 的 Array 对象是用于构造数组的全局对象，数组是类似于列表的高阶对象

## api list

| class                                | api                                                                                                | more                                                                                                                                                       |
| ------------------------------------ | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 创建数组                             | []                                                                                                 | -                                                                                                                                                          |
| ^                                    | new Array()                                                                                        | -                                                                                                                                                          |
| ^                                    | new Array(len)                                                                                     | 创建指定长度的数组                                                                                                                                         |
| Array                                | Array.of(element0[, element1[, ...[, elementN]]])                                                  | 创建一个具有可变数量参数的新数组实例，而不考虑参数的数量或类型（数组元素为 empty）                                                                         |
| ^                                    | Array.from(arrayLike[, mapFn[, thisArg])                                                           | 从一个类似数组或可迭代对象中创建一个新的，浅拷贝的数组实例 (如果对象 length 属性与实际元素个数不相符，空缺的地方为 undefind、多余的部分过滤掉)             |
| ^                                    | Array.isArray(obj)                                                                                 | 用于确定传递的值是否是一个 Array                                                                                                                           |
| Iterator                             | Array.prototype[Symbol.iterator]()                                                                 | @@iterator 属性和 Array.prototype.values() 属性的初始值均为同一个函数对象                                                                                  |
| ^                                    | Array.prototype.entries()                                                                          | 返回一个新的 Array Iterator 对象，该对象包含数组中每个索引的键/值对                                                                                        |
| ^                                    | Array.prototype.keys()                                                                             | 返回一个包含数组中每个索引键的 Array Iterator 对象                                                                                                         |
| ^                                    | Array.prototype.values()                                                                           | 返回一个新的 Array Iterator 对象，该对象包含数组每个索引的值                                                                                               |
| ^                                    | Array.prototype.find(callback[, thisArg])                                                          | 返回数组中满足提供的测试函数的第一个元素的值。否则返回 undefined                                                                                           |
| ^                                    | Array.prototype.findIndex(callback[, thisArg])                                                     | 返回数组中满足提供的测试函数的第一个元素的索引。否则返回-1                                                                                                 |
| Iterator-`empty 跳过`                | Array.prototype.every(callback[, thisArg])                                                         | 测试一个数组内的所有元素是否都能通过某个指定函数的测试。它返回一个布尔值。                                                                                 |
| ^                                    | Array.prototype.filter(callback[, thisArg])                                                        | 创建一个新数组, 其包含通过所提供函数实现的测试的所有元素                                                                                                   |
| ^                                    | Array.prototype.flatMap(callback[, thisArg])                                                       | 首先使用映射函数映射每个元素，然后将结果压缩成一个新数组                                                                                                   |
| ^                                    | Array.prototype.forEach(callback[, thisArg])                                                       | 对数组的每个元素执行一次提供的函数                                                                                                                         |
| ^                                    | Array.prototype.map(callback[, thisArg])                                                           | 创建一个新数组，其结果是该数组中的每个元素都调用一个提供的函数后返回的结果                                                                                 |
| ^                                    | Array.prototype.some(callback[, thisArg])                                                          | 测试是否至少有一个元素可以通过被提供的函数方法。该方法返回一个 Boolean 类型的值。                                                                          |
| ^                                    | Array.prototype.reduce(callback(accumulator, currentValue[, index[, array]])[, initialValue])      | 对数组中的每个元素执行一个由您提供的 reducer 函数(升序执行)，将其结果汇总为单个返回值。                                                                    |
| ^                                    | Array.prototype.reduceRight(callback(accumulator, currentValue[, index[, array]])[, initialValue]) | 接受一个函数作为累加器（accumulator）和数组的每个值（从右到左）将其减少为单个值。                                                                          |
| 增删改数组-`改变原来数组+empty 保留` | Array.prototype.unshift(element1, ..., elementN)                                                   | 将一个或多个元素添加到数组的开头，并返回该数组的新长度                                                                                                     |
| ^                                    | Array.prototype.shift()                                                                            | 从数组中删除第一个元素，并返回该元素的值。此方法更改数组的长度                                                                                             |
| ^                                    | Array.prototype.push(element1, ..., elementN)                                                      | 将一个或多个元素添加到数组的末尾，并返回该数组的新长度                                                                                                     |
| ^                                    | Array.prototype.pop()                                                                              | 从数组中删除最后一个元素，并返回该元素的值。此方法更改数组的长度                                                                                           |
| ^                                    | Array.prototype.splice(start[, deleteCount[, item1[, item2[, ...]]]])                              | 通过删除或替换现有元素或者原地添加新的元素来修改数组,并以数组形式返回被修改的内容。此方法会改变原数组。                                                    |
| ^                                    | Array.prototype.copyWithin(target[, start[, end]])                                                 | 浅复制数组的一部分到同一数组中的另一个位置，并返回它，不会改变原数组的长度                                                                                 |
| ^                                    | Array.prototype.fill(value[, start[, end]])                                                        | 用一个固定值填充一个数组中从起始索引到终止索引内的全部元素。不包括终止索引。                                                                               |
| ^                                    | Array.prototype.reverse()                                                                          | 将数组中元素的位置颠倒,并返回该数组。该方法会改变原数组                                                                                                    |
| ^                                    | Array.prototype.sort([compareFunction])                                                            | 对数组的元素进行排序，并返回数组(`正序倒序 empty 元素都会被排到最后`)                                                                                      |
| 查看-`不改变原来数组`                | Array.prototype.indexOf(searchElement[, fromIndex = 0])                                            | 返回在数组中可以找到一个给定元素的第一个索引，如果不存在，则返回-1                                                                                         |
| ^                                    | Array.prototype.lastIndexOf(searchElement[, fromIndex = arr.length - 1])                           | 返回指定元素（也即有效的 JavaScript 值或变量）在数组中的最后一个的索引，如果不存在则返回 -1。从数组的后面向前查找，从 fromIndex 处开始                     |
| ^                                    | Array.prototype.includes(valueToFind[, fromIndex])                                                 | 用来判断一个数组是否包含一个指定的值，根据情况，如果包含则返回 true，否则返回 false                                                                        |
| ^                                    | Array.prototype.join([separator])                                                                  | 将一个数组（或一个类数组对象）的所有元素连接成一个字符串并返回这个字符串。如果数组只有一个项目，那么将返回该项目而不使用分隔符 (多维数组有问题)            |
| ^                                    | Array.prototype.toString()                                                                         | 返回一个字符串，表示指定的数组及其元素                                                                                                                     |
| ^                                    | Array.prototype.toLocaleString([locales[,options]]))                                               | 返回一个字符串表示数组中的元素。数组中的元素将使用各自的 toLocaleString 方法转成字符串，这些字符串将使用一个特定语言环境的字符串（例如一个逗号 ","）隔开。 |
| 新数组(不改变原来数组)               | Array.prototype.concat(value1[, value2[, ...[, valueN]]]))                                         | 用于合并两个或多个数组或元素。此方法不会更改现有数组，而是返回一个新数组                                                                                   |
| ^                                    | Array.prototype.flat(depth)                                                                        | 按照一个可指定的深度递归遍历数组，并将所有元素与遍历到的子数组中的元素合并为一个新数组返回。(`移除 empty`)                                                 |
| ^                                    | Array.prototype.slice([begin[,end]])                                                               | 返回一个新的数组对象，这一对象是一个由 begin 和 end（不包括 end）决定的原数组的浅拷贝。原始数组不会被改变                                                  |
| 其他                                 | Array.prototype.length                                                                             | 刻意的设置 length 小于数组元素的数量会删除多余的元素，刻意的设置 length 大于数组元素的数量会使数组变为稀疏数组                                             |
| ^                                    | delete arr[index]                                                                                  | 删除数组某个索引处等元素 (`会让相应元素变成稀疏元素 empty`)                                                                                                |
| ^                                    | for...of 循环                                                                                      | `将 empty 转为 undefined`                                                                                                                                  |
| ^                                    | 扩展运算符（...）                                                                                  | ^                                                                                                                                                          |