# Element-Plus 常见问题列表

## 问题1

**报错提示**

```nginx
按需加载 Element-Plus, 在使用 ElMessage(), ElNotification() 等弹窗组件无法展示,但 DOM 节点也确实存在于页面。
`路径: vite.config.js`
import AutoImport from 'unplugin-auto-import/vite';
import Components from 'unplugin-vue-components/vite';
import { ElementPlusResolver } from 'unplugin-vue-components/resolvers';

defineConfig({
	...
	plugins: [
		AutoImport({
	    resolvers: [ElementPlusResolver()],
	  }),
	  Components({
	    dts: true,
	    resolvers: [
	      ElementPlusResolver({
	        importStyle: 'sass',
	      }),
	    ],
	  }),
	]
	...
})
  
```

**解决方案**

```markdown
1. 使用命令式组件弹窗，需要手动加载当前组件的样式，建议手动加载全局样式；
`路径: main.js`
/** 导入 Element-Plus 全局样式, 用于弹窗之类的样式 */
import 'element-plus/dist/index.css';

2. 在当前页面引入弹窗组件
import { ElMessage } from 'element-plus'
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