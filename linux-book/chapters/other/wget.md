# wget

## 命令列表

命令                                                                                                                                          | 含义
------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------
wget xxx                                                                                                                                    | 从网络下载一个文件并保存在当前目录
wget -O wordpress.zip xxx                                                                                                                   | 以特定的文件名保存
wget –limit-rate=300k xxx                                                                                                                   | 限速下载
wget -c xxx                                                                                                                                 | 重新启动下载中断的文件
wget -b xxx                                                                                                                                 | 对于下载非常大的文件的时候，我们可以使用参数-b进行后台下载.你可以使用以下命令来察看下载进度:tail -f wget-log
wget –user-agent="Mozilla/5.0 (Windows; U; Windows NT 6.1; en-US) AppleWebKit/534.16 (KHTML, like Gecko) Chrome/10.0.648.204 Safari/534.16″ | 有些网站能通过根据判断代理名称不是浏览器而拒绝你的下载请求。不过你可以通过–user-agent参数伪装
wget –spider xxx                                                                                                                            | 测试下载链接
wget –tries=40 xxx                                                                                                                          | 如果网络有问题或下载一个大文件也有可能失败。wget默认重试20次连接下载文件。如果需要，你可以使用–tries增加重试次数
wget -i filelist.txt                                                                                                                        | 下载多个文件:cat > filelist.txt url1 url2 url3 url4
wget –mirror -p –convert-links -P ./LOCAL URL                                                                                               | –miror:开户镜像下载 :-p:下载所有为了html页面显示正常的文件 ;–convert-links:下载后，转换成本地的链接;-P ./LOCAL：保存所有文件和目录到本地指定目录
wget –reject=gif xxx                                                                                                                        | 过滤指定格式下载
wget -o download.log xxx                                                                                                                    | 把下载信息存入日志文件
wget -Q5m -i filelist.txt                                                                                                                   | 限制总下载文件大小(对单个文件下载不起作用)
wget -r -A.pdf url                                                                                                                          | 使用wget -r -A下载指定格式文件
wget ftp-xxx                                                                                                                                | 使用wget匿名ftp下载
wget –ftp-user=USERNAME –ftp-password=PASSWORD xxx                                                                                          | 使用wget用户名和密码认证的ftp下载