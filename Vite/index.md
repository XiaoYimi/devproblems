# Vite 常见问题列表

## 问题1

**报错提示**

```nginx
You are running the esm-bundler build of vue-i18n. It is recommended to configure your bundler to explicitly replace feature flag globals with boolean literals to get proper tree-shaking in the final bundle.
```

**解决方案**

```markdown
1. 在 `vite.config.js` 中进行以下配置:
defineConfig({
  resolve: {
    alias: {
      'vue-i18n': 'vue-i18n/dist/vue-i18n.cjs.js',
    }
  }
});
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

