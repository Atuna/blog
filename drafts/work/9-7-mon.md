1. dataview 功能的整体介绍、使用
2. dataview 前端技术栈 √
3. dataview 服务部署管理     

该项目主要以 [UMI][1] + [DVA][2] 为底层框架，以Ant Design(moblie & pc) 为 UI 组件库，包含完整的前端工程化实践。
基于[Ant Design Pro][3]搭建的项目


- 权限管理
- 数据源 -> 数据集 -> 图表组件
- 数据结构参考: /src/types/widget.ts:DataFilter， /api.md
- 看板 -> 图表组件
- EChart，React-Table
- 移动端，PC端，数据大屏

移动端涉及到加密
src/utils/getAppToken.js

[1]: https://v2.umijs.org/zh/guide/
[2]: https://dvajs.com/guide/
[3]: https://v2-pro.ant.design/docs/getting-started-cn