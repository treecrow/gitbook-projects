# [RegExp](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/RegExp)

> RegExp 构造函数创建了一个正则表达式对象，用于将文本与一个模式匹配

## 相关文档

- [javascript 指南-正则表达式](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions)
- [正则表达式 30 分钟入门教程](https://deerchao.net/tutorials/regex/regex.htm)
- [regex101(在线正则表达式开发)](https://regex101.com/)

## api list

| class              | api                                                           | more                                                                                                                                                                                      |
| ------------------ | ------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 创建正则表达式对象 | /pattern/flags                                                | 字面量方式                                                                                                                                                                                |
| ^                  | new RegExp(pattern [, flags])                                 | RegExp 构造函数方式                                                                                                                                                                       |
| ^                  | RegExp(pattern [, flags])                                     | -                                                                                                                                                                                         |
| 修饰符             | g                                                             | 全局匹配;找到所有匹配，而不是在第一个匹配后停止                                                                                                                                           |
| ^                  | i                                                             | 忽略大小写                                                                                                                                                                                |
| ^                  | m                                                             | 多行; 将开始和结束字符（^和\$）视为在多行上工作（也就是，分别匹配每一行的开始和结束（由 \n 或 \r 分割），而不只是只匹配整个输入字符串的最开始和最末尾处                                   |
| ^                  | u                                                             | Unicode; 将模式视为 Unicode 序列点的序列                                                                                                                                                  |
| ^                  | y                                                             | 粘性匹配; 仅匹配目标字符串中此正则表达式的 lastIndex 属性指示的索引(并且不尝试从任何后续的索引匹配)                                                                                       |
| 属性               | RegExp.prototype.global                                       | 布尔值,表示是否设置了 g 标志                                                                                                                                                              |
| ^                  | RegExp.prototype.ignoreCase                                   | 布尔值,表示是否设置了 i 标志                                                                                                                                                              |
| ^                  | RegExp.prototype.multiline                                    | 布尔值,表示是否设置了 m 标志                                                                                                                                                              |
| ^                  | RegExp.prototype.sticky                                       | 布尔值,表示是否设置了 y 修饰符                                                                                                                                                            |
| ^                  | RegExp.prototype.dotAll                                       | 布尔值,表示是否设置了 s 修饰符                                                                                                                                                            |
| ^                  | RegExp.prototype.flags                                        | 返回正则表达式的修饰符                                                                                                                                                                    |
| ^                  | RegExp.prototype.source                                       | 返回正则表达式的正文                                                                                                                                                                      |
| ^                  | RegExp.prototype.lastIndex                                    | 整数,表示开始搜索下一个匹配项的字符位置,从 0 算起                                                                                                                                         |
| 方法               | RegExp.prototype.exec(str) `与 String.prototype.match 类似`   | 如果匹配成功，exec() 方法返回一个数组，并更新正则表达式对象的属性。返回的数组将完全匹配成功的文本作为第一项，将正则括号里匹配成功的作为数组填充到后面。如果匹配失败，exec() 方法返回 null |
| ^                  | RegExp.prototype.test(str)                                    | 测试当前正则是否能匹配目标字符串。                                                                                                                                                        |
| ^                  | RegExp.prototype.toString()                                   | 返回一个字符串，其值为该正则对象的字面量形式                                                                                                                                              |
| ^                  | RegExp.prototype.toLocalString()                              | 返回字符串形式的正则表达式                                                                                                                                                                |
| ^                  | RegExp.prototype.valueOf()                                    | -                                                                                                                                                                                         |
| String             | String.prototype.match(regexp)                                | 检索返回一个字符串匹配正则表达式的的结果:[第一个匹配项目[,第二个匹配项目][,第n个匹配项目],index:, input:, groups:]                                                                        |
| ^                  | `String.prototype.replace(regexp|substr, newSubStr|function)` | 返回一个由替换值（replacement）替换一些或所有匹配的模式（pattern）后的新字符串                                                                                                            |
| ^                  | String.prototype.search(regexp)                               | 执行正则表达式和 String 对象之间的一个搜索匹配                                                                                                                                            |
| ^                  | String.prototype.split([separator[, limit]])                  | 使用指定的分隔符字符串将一个 String 对象分割成字符串数组，以将字符串分隔为子字符串，以确定每个拆分的位置                                                                                  |

## 正则表达式中的特殊字符

| class          | 字符            | 含义                                                                                                                                                                       |
| -------------- | --------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 字符类别       | `.`             | 匹配除换行符以外的任意字符                                                                                                                                                 |
| ^              | `\d`            | 匹配任意阿拉伯数字。等价于[0-9]                                                                                                                                            |
| ^              | `\D`            | 匹配任意一个不是阿拉伯数字的字符。等价于[^0-9]                                                                                                                             |
| ^              | `\w`            | 匹配任意来自基本拉丁字母表中的字母数字字符，还包括下划线。等价于 [A-Za-z0-9_]                                                                                              |
| ^              | `\W`            | 匹配任意不是基本拉丁字母表中单词（字母数字下划线）字符的字符。等价于 [^a-za-z0-9_]                                                                                         |
| ^              | `\s`            | 匹配一个空白符，包括空格、制表符、换页符、换行符和其他 Unicode 空格                                                                                                        |
| ^              | `\S`            | 匹配一个非空白符。等价于 [^ \f\n\r\t\v​\u00a0\u1680​\u180e\u2000​\u2001\u2002​\u2003\u2004​ \u2005\u2006​\u2007\u2008​\u2009\u200a​\u2028\u2029​\u202f\u205f​\u3000]       |
| ^              | `\t`            | 匹配一个水平制表符                                                                                                                                                         |
| ^              | `\r`            | 匹配一个回车符                                                                                                                                                             |
| ^              | `\n`            | 匹配一个换行符                                                                                                                                                             |
| ^              | `\v`            | 匹配一个垂直制表符                                                                                                                                                         |
| ^              | `\f`            | 匹配一个换页符                                                                                                                                                             |
| ^              | `[\b]`          | 匹配一个退格符（不要与 \b 混淆）                                                                                                                                           |
| ^              | `\0`            | 匹配一个 NUL 字符                                                                                                                                                          |
| ^              | `\cX`           | X 是 A - Z 的一个字母。匹配字符串中的一个控制字符                                                                                                                          |
| ^              | `\xhh`          | 匹配编码为 hh （两个十六进制数字）的字符                                                                                                                                   |
| ^              | `\uhhhh`        | 匹配 Unicode 值为 hhhh （四个十六进制数字）的字符                                                                                                                          |
| 字符集合       | `[xyz]`         | 一个字符集合，也叫字符组。匹配集合中的任意一个字符。你可以使用连字符'-'指定一个范围                                                                                        |
| ^              | `[^xyz]`        | 一个反义或补充字符集，也叫反义字符组                                                                                                                                       |
| 边界           | `^`             | 匹配输入开始                                                                                                                                                               |
| ^              | `\$`            | 匹配输入结尾                                                                                                                                                               |
| ^              | `\b`            | 匹配一个零宽单词边界（zero-width word boundary），如一个字母与一个空格之间                                                                                                 |
| ^              | `\B`            | 匹配一个零宽非单词边界（zero-width non-word boundary），如两个字母之间或两个空格之间                                                                                       |
| 数量词         | `x*`            | 匹配前面的模式 x 0 或多次(任意次)                                                                                                                                          |
| ^              | `x+`            | 匹配前面的模式 x 1 或多次。等价于 {1,}                                                                                                                                     |
| ^              | `x*?` and `x+?` | 像上面的 `*` 和 + 一样匹配前面的模式 x，然而匹配是最小可能匹配                                                                                                             |
| ^              | `x?`            | 匹配前面的模式 x 0 或 1 次                                                                                                                                                 |
| ^              | `x{n}`          | n 是一个正整数。前面的模式 x 连续出现 n 次时匹配                                                                                                                           |
| ^              | `x{n,}`         | n 是一个正整数。前面的模式 x 连续出现至少 n 次时匹配                                                                                                                       |
| ^              | `x{n,m}`        | n 和 m 为正整数。前面的模式 x 连续出现至少 n 次，至多 m 次时匹配                                                                                                           |
| ^              | `x|y`           | 匹配 x 或 y                                                                                                                                                                |
| 前后断言       | `x(?=y)`        | 只有当 x 后面紧跟着 y 时，才匹配 x                                                                                                                                         |
| ^              | `x(?!y)`        | 只有当 x 后面不是紧跟着 y 时，才匹配 x                                                                                                                                     |
| ^              | `(?<=y)x`       | 后行断言，x 只有在 y 后面才匹配                                                                                                                                            |
| ^              | `(?<!y)x`       | 后行否定断言,x 只有不在 y 后面才匹配                                                                                                                                       |
| 分组与反向引用 | `(x)`           | 匹配 x 并且捕获匹配项。 这被称为捕获括号                                                                                                                                   |
| ^              | `\n`            | n 是一个正整数。一个反向引用（back reference），指向正则表达式中第 n 个括号（从左开始数）中匹配的子字符串                                                                  |
| ^              | `(?:x)`         | 匹配 x 不会捕获匹配项。这被称为非捕获括号（non-capturing parentheses）。匹配项不能够从结果数组的元素 [1], ..., [n] 或已被定义的 RegExp 对象的属性 $1, ..., $9 再次访问到。 |
| orther         | \               | 使用`\`可以将不同匹配规则分开,只要满足了其中一个就可以                                                                                                                     |
| ^              | `(...)`         | 将单独的项组合成子表达式： /java(script)?/                                                                                                                                 |
| ^              | `(...)`         | 在完整的模式中定义子模式: /[a-z]+(\d+)/                                                                                                                                    |
| ^              | `(...)`         | 在同一正则表达式的后部引用前面的子表达式： /(['"])[^'"]\*\1/                                                                                                               |
| ^              | `(?<year>)`     | 具名组匹配(结合 exec 方法)                                                                                                                                                 |
| ^              | `\e`            | escape 字符                                                                                                                                                                |
| ^              | `\a`            | alert 字符                                                                                                                                                                 |  |
| ^              | `\p{...}`       | 允许正则表达式匹配符合 Unicode 某种属性的所有字符                                                                                                                          |
| ^              | `\P{...}`       | `\P{…}`是`\p{…}`的反向匹配，即匹配不满足条件的字符                                                                                                                         |

## 常用正则列表

| class | name             | 正则                                                                              | more                                              |
| ----- | ---------------- | --------------------------------------------------------------------------------- | ------------------------------------------------- |
| 校验  | is_name          | `/^[a-zA-Z\u4e00-\u9fa5\·]{2,}$/`                                                 | 姓名由大小写英文字母、汉字、·组成，长度不能小于 2 |
| ^     | is_email         | `/^([a-zA-Z0-9_\-\.]+@[a-zA-Z0-9_\-\.]+\.[a-zA-Z]{2,})$/`                         | -                                                 |
| ^     | is_phone         | `/^1[3|4|5|6|7|8|9][0-9]{9}$/`                                                    | -                                                 |
| ^     | is_tel_phone     | `/^((0\d{2,3})-)(\d{7,8})(-(\d{3,}))?$/`                                          | -                                                 |
| ^     | is_captcha       | `/^[0-9a-zA-Z]{6}$/`                                                              | 大小写英文字母、数字组成，长度 6 位               |
| ^     | is_pwd           | `/^[a-zA-Z0-9!@#$%^&*()-+=~:()><,.'?\"]{6,20}$/`                                  | 数字字母符号混合密码，长度 6-20 位                |
| ^     | is_qq            | `/^[1-9]\d{6,20}$/`                                                               | 首位不为 0                                        |
| 获取  | get_extensions   | `/[^.]+$/.exec(filename)[0]`                                                      | 获取文件扩展名                                    |
| ^     | get_char_length  | `str.split(/[aeiou]/gi).length - 1`                                               | 获取指定字符个数                                  |
| 转换  | rm_non_cn        | `str.replace(/[^\u4e00-\u9fa5]/g, "")`                                            | 过滤非中文                                        |
| ^     | turn_underline   | `str.replace(/([A-Z])/g, "_$1").toLowerCase()`                                    | 驼峰格式转化为下划线                              |
| ^     | turn_hump        | `str.replace(/_(\w)/g, ($0, $1) => $1.toUpperCase())`                             | 下划线转化为驼峰格式                              |
| ^     | upper_first_char | `str.replace(/\b(\w)(\w*)/g,($0, $1, $2) => $1.toUpperCase() + $2.toLowerCase())` | 首字母大写                                        |