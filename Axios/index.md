# Axios 常见问题列表

## 问题1

**报错提示**

```nginx
GET http://192.168.2.5:3000/ net::ERR_CONNECTION_REFUSED
```

**解决方案**

```markdown
1. 后端服务未启动(让后端启动服务)
2. 访问失败(让后端检查服务)
```



## 问题2

**报错提示**

```nginx
Access to XMLHttpRequest at 'http://192.168.2.3:3000/' from origin 'http://192.168.2.3:8080' has been blocked by CORS policy: The value of the 'Access-Control-Allow-Origin' header in the response must not be the wildcard '*' when the request's credentials mode is 'include'. The credentials mode of requests initiated by the XMLHttpRequest is controlled by the withCredentials attribute.
```

**解决方案**

```markdown
1. 出现跨域请求(请参考跨域请求解决方案)。
2. 后端服务已允许跨域请求,可能由于 axios 配置设置 `withCredentials = true`。 
```



## 问题编号

**报错提示**

```nginx
报错提示
```

**解决方案**

```markdown
1. 解决方案描述1
2. 解决方案描述2
```

