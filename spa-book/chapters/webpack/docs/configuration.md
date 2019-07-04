# [configuration](https://webpack.js.org/configuration/)

## configuration list

| class                                                                    | option                                       | more                                                                                                                            |
| ------------------------------------------------------------------------ | -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| [mode](https://webpack.js.org/configuration/mode/)                       | mode                                         | 提供模式配置选项会告诉 Webpack 相应地使用其内置优化                                                                             |
| [Entry and Context](https://webpack.js.org/configuration/entry-context/) | -                                            | -                                                                                                                               |
| ^                                                                        | context                                      | Webpack 在寻找相对路径的文件时会以 context 为根目录，context 默认为执行启动 Webpack 时所在的当前工作目录                        |
| ^                                                                        | entry                                        | webpack 开始构建捆绑包的地方                                                                                                    |
| [Output](https://webpack.js.org/configuration/output/)                   | -                                            | 顶级 output 键包含一组选项，用于指示 webpack 如何以及在何处输出您的包，静态文件以及您使用 webpack 捆绑或加载的任何其他内容      |
| ^                                                                        | output.path                                  | The output directory as an absolute path                                                                                        |
| ^                                                                        | output.filename                              | This option determines the name of each output bundle                                                                           |
| ^                                                                        | output.chunkFilename                         | 确定非入口块文件的名称                                                                                                          |
| ^                                                                        | output.publicPath                            | 指定在浏览器中引用时输出目录的公共 URL                                                                                          |
| ^                                                                        | output.library                               | How the value of the output.library is used depends on the value of the output.libraryTarget option                             |
| ^                                                                        | output.libraryTarget                         | Configure how the library will be exposed                                                                                       |
| ^                                                                        | output.auxiliaryComment                      | -                                                                                                                               |
| ^                                                                        | output.chunkLoadTimeout                      | -                                                                                                                               |
| ^                                                                        | output.crossOriginLoading                    | -                                                                                                                               |
| ^                                                                        | output.jsonpScriptType                       | -                                                                                                                               |
| ^                                                                        | output.devtoolFallbackModuleFilenameTemplate | -                                                                                                                               |
| ^                                                                        | output.devtoolLineToLine                     | -                                                                                                                               |
| ^                                                                        | output.devtoolModuleFilenameTemplate         | -                                                                                                                               |
| ^                                                                        | output.devtoolNamespace                      | -                                                                                                                               |
| ^                                                                        | output.globalObject                          | -                                                                                                                               |
| ^                                                                        | output.hashDigest                            | -                                                                                                                               |
| ^                                                                        | output.hashDigestLength                      | -                                                                                                                               |
| ^                                                                        | output.hashFunction                          | -                                                                                                                               |
| ^                                                                        | output.hashSalt                              | -                                                                                                                               |
| ^                                                                        | output.hotUpdateChunkFilename                | -                                                                                                                               |
| ^                                                                        | output.hotUpdateFunction                     | -                                                                                                                               |
| ^                                                                        | output.hotUpdateMainFilename                 | -                                                                                                                               |
| ^                                                                        | output.jsonpFunction                         | -                                                                                                                               |
| ^                                                                        | output.libraryExport                         | -                                                                                                                               |
| ^                                                                        | output.pathinfo                              | -                                                                                                                               |
| ^                                                                        | output.sourceMapFilename                     | -                                                                                                                               |
| ^                                                                        | output.sourcePrefix                          | -                                                                                                                               |
| ^                                                                        | output.strictModuleExceptionHandling         | -                                                                                                                               |
| ^                                                                        | output.umdNamedDefine                        | -                                                                                                                               |
| ^                                                                        | output.futureEmitAssets                      | -                                                                                                                               |
| [Module](https://webpack.js.org/configuration/module/)                   | -                                            | 决定如何处理项目中不同类型的模块                                                                                                |
| ^                                                                        | module.noParse                               | 阻止 Webpack 处理与给定正则表达式匹配的任何文件                                                                                 |
| ^                                                                        | module.rules                                 | An array of Rules which are matched to requests when modules are created                                                        |
| ^                                                                        | module.someRule.test                         | Rule.test is a shortcut to Rule.resource.test                                                                                   |
| ^                                                                        | module.someRule.exclude                      | 同样是一个字符串或者字符串数组，指定目录中的文件不需要走这个规则                                                                |
| ^                                                                        | module.someRule.include                      | 是一个字符串或者字符串数组，指定目录中的文件需要走这个规则                                                                      |
| ^                                                                        | module.someRule.resource                     | 就是对 text/include/exclude 的一个对象包装，和他们单独写没有区别                                                                |
| ^                                                                        | module.someRule.issuer                       | 和 resource 有异曲同工的作用，不过区别在于它是将这个 rule 应用于哪个文件以及这个文件所导入的所有依赖文件                        |
| ^                                                                        | module.someRule.resourceQuery                | 和 resource 用法一样，不过针对的是匹配结果'?'后面的路径参数，可以调用 resource 中的 text 等                                     |
| ^                                                                        | module.someRule.oneOf                        | 表示对该资源只应用第一个匹配的规则                                                                                              |
| ^                                                                        | module.someRule.use                          | 是对 useEntry 的集合，并且对每一个入口指定使用一个 loader                                                                       |
| ^                                                                        | module.someRule.loaders                      | Rule.loaders is an alias to Rule.use                                                                                            |
| ^                                                                        | module.someRule.loader                       | Rule.loader is a shortcut to Rule.use: [ { loader } ]                                                                           |
| ^                                                                        | module.someRule.enforce                      | -                                                                                                                               |
| ^                                                                        | module.someRule.options                      | -                                                                                                                               |
| ^                                                                        | module.someRule.parser                       | -                                                                                                                               |
| ^                                                                        | module.someRule.rules                        | -                                                                                                                               |
| ^                                                                        | module.someRule.sideEffects                  | -                                                                                                                               |
| ^                                                                        | module.someRule.type                         | -                                                                                                                               |
| [externals](https://webpack.js.org/configuration/externals/)             | -                                            | 提供一种从输出包中排除依赖项的途径                                                                                              |
| [Optimization](https://webpack.js.org/configuration/optimization/)       | -                                            | webpack4 根据 mode 选项为打包做优化，同时也可以通过 optimizations 手动优化打包流程                                              |
| ^                                                                        | optimization.splitChunks                     | 代码分割                                                                                                                        |
| ^                                                                        | optimization.runtimeChunk                    | Setting optimization.runtimeChunk to true or "multiple" adds an additional chunk to each entrypoint containing only the runtime |
| ^                                                                        | optimization.minimize                        | -                                                                                                                               |
| ^                                                                        | optimization.minimizer                       | -                                                                                                                               |
| ^                                                                        | optimization.noEmitOnErrors                  | -                                                                                                                               |
| ^                                                                        | optimization.namedModules                    | -                                                                                                                               |
| ^                                                                        | optimization.namedChunks                     | -                                                                                                                               |
| ^                                                                        | optimization.moduleIds                       | -                                                                                                                               |
| ^                                                                        | optimization.chunkIds                        | -                                                                                                                               |
| ^                                                                        | optimization.nodeEnv                         | -                                                                                                                               |
| ^                                                                        | optimization.mangleWasmImports               | -                                                                                                                               |
| ^                                                                        | optimization.removeAvailableModules          | -                                                                                                                               |
| ^                                                                        | optimization.removeEmptyChunks               | -                                                                                                                               |
| ^                                                                        | optimization.mergeDuplicateChunks            | -                                                                                                                               |
| ^                                                                        | optimization.flagIncludedChunks              | -                                                                                                                               |
| ^                                                                        | optimization.occurrenceOrder                 | -                                                                                                                               |
| ^                                                                        | optimization.providedExports                 | -                                                                                                                               |
| ^                                                                        | optimization.usedExports                     | -                                                                                                                               |
| ^                                                                        | optimization.concatenateModules              | -                                                                                                                               |
| ^                                                                        | optimization.sideEffects                     | -                                                                                                                               |
| ^                                                                        | optimization.portableRecords                 | -                                                                                                                               |