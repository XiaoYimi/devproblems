# Vue 常见问题列表

## 问题1

**报错提示**

```nginx
[Vue warn]: inject() can only be used inside setup() or functional components.
```

**解决方案**

```markdown
1. 在 Vuex 中,全局状态管理模式是分层管理(modules,默认一层)的。除了 `template`，`script setup` 外，想获取全局状态管理的缓存数据,内部会使用到 inject 方法，从而导致该问题触发。所以不要在函数内部函数中使用 `store = useStore()` 或者 `useStore()`，这样就可以避免该问题触发。
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