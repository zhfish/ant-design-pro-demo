# Issues专用
https://github.com/ant-design/ant-design-pro/issues/6219
## 环境
- Macos 10.15.3
- Edge 81
## 已经做过的操作
1. npm create umi
2. npm i
3. npm run i18n-remove
4. `Welcome.tsx`里添加Button：`触发Modal.Api`
5. `config/config.ts`里把`Welcome.icon`的内容替换成`SendOutline`
6. `SendOutline`可以在antd的icon组件里找到
## 复现
1. npm run start
## 问题
1. 按钮是英文`Cancel`,`OK`
2. Console提示警告
```
Warning: The current popular language does not exist, please check the locales folder!
```
3. Console提示警告
```index.js:1 Warning: In order to ensure compatibility with antd@4, we will delete the configuration icon in the next version, details can be viewed.
为了兼容 antd@4，我们会在下个版本删除配置 icon: string 生成icon的用法。请查看
https://pro.ant.design/blog/antd-4.0-cn 寻找解决方式
```

4. 左侧Menu没有显示icon，而是显示了icon的string

## 期望结果

1. 较低的预期是Config里`locale.antd=true`时，Modal.confrim的按钮可以是中文
2. 较高的预期是Config里`locale.antd=false`时，antd控件可以被指定为`locale.default`的语言，并且不提示`language does not exist`警告
3. `umi-plugin-antd-icon-config`可以正常生效，或者`menu.icon`可以传入ReactNode，没必要非得string
