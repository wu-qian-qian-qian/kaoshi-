# 在线考试系统 v1.8 - GitHub Pages 部署版

## 🚀 快速部署到 GitHub Pages

### 1. 创建 GitHub 仓库

1. 访问 [GitHub](https://github.com)
2. 点击 "New repository"
3. 填写仓库信息：
   - Repository name: `exam-system`（或您喜欢的名字）
   - Description: `在线考试系统`
   - 选择 "Public"（必须公开才能使用 GitHub Pages）
   - 勾选 "Add a README file"
4. 点击 "Create repository"

### 2. 上传文件

1. 将 `github-pages-deploy` 文件夹中的所有文件上传到仓库
2. 确保文件在仓库的根目录下

### 3. 启用 GitHub Pages

1. 进入仓库的 "Settings" 页面
2. 滚动到 "Pages" 部分
3. 在 "Source" 下选择 "Deploy from a branch"
4. 选择 "main" 分支和 "/ (root)" 文件夹
5. 点击 "Save"

### 4. 获取访问链接

部署完成后，您的考试系统将在以下地址可用：
```
https://您的用户名.github.io/您的仓库名/cloud-exam-system.html
```

学生端访问地址：
```
https://您的用户名.github.io/您的仓库名/cloud-exam.html
```

## 🌐 配置云端存储

### 1. 设置 JSONBin.io

1. 访问 [JSONBin.io](https://jsonbin.io/)
2. 注册账号并登录
3. 创建新的 Bin，内容：`{"exams":[],"results":[]}`
4. 复制 Bin URL 和 Secret Key

### 2. 配置管理后台

1. 访问管理后台：`https://您的用户名.github.io/您的仓库名/cloud-exam-system.html`
2. 在"云端配置"面板中填入：
   - Bin URL：从 JSONBin.io 复制的 URL
   - Secret Key：从 JSONBin.io 复制的 Secret Key
3. 点击"测试连接"确认配置成功
4. 点击"保存配置"

### 3. 更新配置文件

配置成功后，系统会自动生成 `cloud-config.json` 文件，请确保此文件在仓库根目录下。

## 📱 使用方法

### 管理员操作

1. **创建考试**：
   - 在管理后台点击"管理后台"
   - 填写考试名称和允许的考号
   - 点击"创建新考试"

2. **添加题目**：
   - 选择已创建的考试
   - 可以手动添加题目或导入 Excel 文件
   - 点击"发布考试"使考试对学生可见

3. **查看结果**：
   - 点击"查看结果"查看所有考试结果
   - 点击"详细分析"查看每道题的答题情况
   - 支持导出分析数据到 Excel

### 学生操作

1. **参加考试**：
   - 访问学生端链接
   - 输入考号验证身份
   - 填写个人信息
   - 选择考试并开始答题

2. **查看结果**：
   - 提交试卷后立即显示成绩
   - 可以重新开始新的考试

## 🔧 技术特性

- **云端同步**：使用 JSONBin.io 实现数据云端同步
- **响应式设计**：支持手机、平板、电脑访问
- **实时更新**：管理员和学生端数据实时同步
- **数据导出**：支持 Excel 格式的数据导出
- **安全验证**：考号验证确保考试安全

## 📞 支持

如有问题，请检查：
1. GitHub Pages 是否正常部署
2. JSONBin.io 配置是否正确
3. 浏览器控制台是否有错误信息

## 🎯 优势

- **全球访问**：任何网络环境都能访问
- **无需服务器**：完全基于 GitHub Pages
- **免费使用**：GitHub Pages 和 JSONBin.io 都免费
- **自动备份**：数据自动保存到云端
- **易于维护**：代码托管在 GitHub，便于版本管理
