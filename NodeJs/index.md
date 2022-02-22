# NodeJs 常见问题列表

## 问题编号

**报错提示**

```nginx
UnhandledPromiseRejectionWarning: TypeError [ERR_INVALID_ARG_TYPE]: The "path" argument must be one of type string, Buffer, or URL.
```

**解决方案**

```markdown
1. 这是由于在调用 Node 内置模块方法时,传参不正确导致的。因为该参数 `path` 只接收 string, Buffer, or URL 这三种类型值.比如 Node 内置模块 `fs` 调用方法 `stat`, 第一个参数 `path` 你传值 `object` 类型值, 就会报此错误。 这时候只要根据 Node 开发文档按要求传值即可.
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
