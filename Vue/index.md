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
[Vue warn]: Property "menu" was accessed during render but is not defined on instance.
```

在 script setup 中通过定义组件接收 props 参数:
defineProps({
  menu: {
    type: Object,
    required: true,
  },
});

但在 template 中使用 :menu="menu" 或者 :menu="$props.menu" 报错;
**解决方案**

```markdown
1. 在 script setup 中应当这样定义组件接收 props 参数:
const myprops = defineProps({
  menu: {
    type: Object,
    required: true,
  },
});
在 template 中使用应当这样使用 :menu="myprops.menu" 即可。
2. 解决方案描述2
```



## 问题3

**报错提示**

```nginx
expected selector.
 
  .el-sub-menu.is-opened /deep/ .el-menu-item.is-active,
                           ^
 
src\cores\layout\components\aside-menu\index.vue 35:26  root stylesheet
```

**解决方案**

```markdown
1. 常见于覆盖组件样式(使用框架组件,或者递归组件)等情况; 一般可通过 >>>, /deep/, v::deep 进行样式穿透解决此类问题; Vue3 中建议使用 v::deep。
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