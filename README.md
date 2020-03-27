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

## 复现
1. npm run start
## 问题
1. 按钮是英文`Cancel`,`OK`
2. Console提示警告
```
Warning: The current popular language does not exist, please check the locales folder!
```
## 期望结果

1. 较低的预期是Config里`locale.antd=true`时，Modal.confrim的按钮可以是中文
2. 较高的预期是Config里`locale.antd=false`时，antd控件可以被指定为`locale.default`的语言，并且不提示`language does not exist`警告

