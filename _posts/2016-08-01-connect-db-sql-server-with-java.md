---
layout: post
title: java与sql server2014中的数据库相连异常
category: thinking
---
1、java.lang.ClassNotFoundException: com.microsoft.jdbc.sqlserver.SQLServerDriver：

需要下载sqljdbc4.jar包并放在bin目录下

<!--more-->
2、com.microsoft.sqlserver.jdbc.SQLServerException: Login failed for user 'sa'.(系统采取了windows模式)：

由于最开始一直是以"windows授权"的模式登录的，所以需要进行以下操作：

1）利用windows授权登录数据库

2）"Object"(右键)-->"Properties"-->"Security"-->"Server authentication"-->"SQL Server and Windows Authentication mode"

3）若“Object”-->“Security”-->"Logins"-->“sa”有红色标志，表明"sa"处于“禁用”状态，此时“sa”(右键)-->"Status"-->"Login"-->"Enabled"

4）重启后利用“SQL Server Authentication”模式登录




[GitHub]: https://github.com/
[jekyll]: https://github.com/mojombo/jekyll
[Markdown]: http://daringfireball.net/projects/markdown/
[WordPress]: http://wordpress.org/
[Disqus]: http://disqus.com/
[Google Picasa]: https://picasaweb.google.com/
[Google Custom Search]: http://www.google.com/cse/
[HighlightJS]: http://softwaremaniacs.org/soft/highlight/en/
[Gravatar]: http://en.gravatar.com/
