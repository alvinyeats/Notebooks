
## Targets
- burpsuite
- awvs
- appscan
- webvulscan
- Arachni

## 安装&使用方法

- burpsuite: 已知
- awvs: [下载地址](https://www.arvinhk.com/post/306.html)，双击安装包进行安装，然后访问 https://localhost:3443 ，执行扫描时会提示需要activate，这时候点击keygen程序
- webvulscan: 将源码包拷贝至xampp/htdocs目录下，访问  http://127.0.0.1/webvulscan/ 
- Arachni: 下载源码，进入bin目录，执行<code>.\arachni_web.bat</code>，访问  http://localhost:9292
- appscan: 进行中

### 默认账号

awvs: 安装过程中注册   
webvulscan: 安装完毕后，在web页面进行注册  

Arachni
```code
Administrator account

E-mail: admin@admin.admin
Password: administrator

Regular user account

E-mail: user@user.user
Password: regular_user
```

## 注意事项

- 开全局代理会导致B/S架构的扫描器无法访问，所以测试是需关闭全局代理
