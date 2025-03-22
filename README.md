# 乐加会年度报告 H5

## 项目简介
这是一个模仿网易云音乐年度报告风格的H5页面，专为乐加会用户定制的2023年度回顾。通过垂直滑动的方式展示用户一年来在乐加会平台的活动数据和成就。

## 页面结构
项目包含 9 个主要页面：

1. **封面页**
   - 展示年度报告标题
   - 简约设计风格
   - 上滑提示动画
   - 动态棕色背景光效
   - 磨砂玻璃效果装饰

2. **加入天数页**
   - 显示会员加入时间
   - 包含日历组件，高亮显示加入日期
   - 展示累计天数和扫码天数数据圈
   - 浮动动画效果

3. **进货统计页（品牌分布）**
   - 展示品牌偏好分析
   - 包含柱状图可视化
   - 显示进货总量和品牌覆盖数
   - 最爱品牌数据圈
   - 浮动动画效果

4. **进货统计页**
   - 简化版进货数据展示
   - 大数字展示进货总量
   - 包含扫码引导按钮

5. **活动参与页**
   - 展示活动参与情况
   - 区分已参与和错过的活动
   - 包含开启通知提醒功能
   - 获得奖励数据圈（含奖励详情列表）
   - 错过活动数据圈（含错过活动列表）

6. **积分统计页（未使用）**
   - 展示积分累计情况
   - 显示未兑换状态
   - 引导访问积分商城

7. **积分统计页**
   - 展示积分使用情况
   - 包含礼品展示区域
   - 显示兑换次数和偏好
   - 最爱礼品数据圈

8. **货券统计页**
   - 按月份展示货券数据
   - 包含累计金额统计
   - 展示等价瓶数转换
   - 兑换次数和抵扣金额数据圈

9. **年度总结页**
   - 展示会员年度形象（鸡尾酒杯图标）
   - 汇总各项数据指标
   - 提供保存和领奖功能
   - 个性化鸡尾酒推荐
   - 年度感谢语
   - 分享按钮（静态展示）

## 设计特点
- 采用线框设计风格
- 黑白主色调，保留橙色作为强调色
- 移动端优先的响应式设计
- 统一的动画效果
- 清晰的数据可视化
- iPhone样式的UI框架（刘海屏和底部指示条）
- 磨砂玻璃特效（backdrop-filter）

### 数据展示效果
- **数据圈设计**
  - 响应式网格布局，支持自适应列数
  - 圆形展示布局
  - 磨砂玻璃背景效果
  - 渐变文字效果
  - 错落动画延迟
  - 悬浮放大效果
  - 优化的点击状态反馈

### 动画系统
- fadeInUp：元素从下方淡入
- floatCircle：元素上下浮动
- pulseScale：元素缩放脉动
- slideIn：元素从左侧滑入
- 页面切换重置动画
- 交错动画延迟

## 技术特点
1. **样式设计**
   - 使用 CSS 变量管理主题色
   - 响应式布局
   - 优雅的动画过渡
   - 适配深色模式

2. **交互设计**
   - 页面序号导航
   - 手势友好的界面
   - 清晰的视觉反馈
   - Swiper实现垂直滑动切换效果

3. **性能优化**
   - 优化的动画性能
   - 响应式图片处理
   - 移动端适配

## 设备适配
- 设计宽度：393px（iPhone 14 Pro）
- 设计高度：852px
- 安全区域：顶部 59px，底部 34px
- 自适应缩放支持其他设备
- 针对小屏设备的特殊处理

## 图片生成功能
- 使用 `bobo_agent.py` 生成鸡尾酒图片
- 支持手动输入模式：
  - 鸡尾酒名称（用作文件名）
  - 图片生成提示词
- 生成的图片自动保存到 `image/summary_images/` 目录

## 开发环境
### 依赖项
- Swiper v11（滑动切换效果）
- Font Awesome 6.5.1（图标库）
- 系统默认字体
- Node.js（可选，用于开发）
- Python 3.x（用于图片生成功能）
- Git（版本控制）

### 环境变量配置
在项目根目录创建 `.env` 文件：
```
SILICONFLOW_TOKEN=your_token_here
FIGMA_ACCESS_TOKEN=your_token_here
```

## 浏览器支持
- 支持现代浏览器（支持 CSS Grid、Flexbox、CSS Variables）
- 针对 iOS Safari 优化
- 支持深色模式

## 使用说明
### 本地开发
1. 安装依赖：
```bash
npm install
```

2. 启动本地服务：
```bash
npm start
```

3. 访问 http://localhost:3000 查看效果

### 生成鸡尾酒图片
1. 运行命令：
```bash
python3 image/bobo_agent.py
```
2. 根据提示输入信息
3. 等待图片生成和下载完成

### Vercel 部署
1. Fork 本项目到自己的 GitHub 仓库
2. 在 Vercel 中导入该仓库
3. 部署时会自动使用项目根目录的配置

## 注意事项
1. 图片生成需要确保 SiliconFlow API Token 有效
2. 不要将 `.env` 文件提交到版本控制系统中
3. 部分CSS特性（如backdrop-filter）可能在旧版浏览器中不支持
4. 页面设计基于iPhone尺寸，在其他设备上会自动缩放适配
