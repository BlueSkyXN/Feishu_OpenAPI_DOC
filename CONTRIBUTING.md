# 贡献指南 | Contributing Guide

感谢您对飞书 OpenAPI 文档库的关注！本项目欢迎所有形式的贡献。

Thank you for your interest in the Feishu OpenAPI Documentation! We welcome all forms of contributions.

---

## 🎯 贡献方式 (How to Contribute)

### 1. 报告问题 (Report Issues)
- 发现文档错误、过时内容或失效链接
- 建议新增或改进文档内容
- 提出项目结构或组织方式的改进建议

### 2. 提交改进 (Submit Improvements)
- 修正文档中的错误或不准确内容
- 更新过时的 API 说明
- 改进文档的可读性和格式
- 添加缺失的文档内容

### 3. 协助维护 (Help Maintain)
- 定期检查并更新文档
- 验证 API 接口的有效性
- 改进文档的组织结构

---

## 📝 文档规范 (Documentation Standards)

### 文件命名规范 (File Naming Convention)

1. **使用中文命名**: 便于理解和查找
2. **避免空格**: 使用下划线 `_` 分隔英文和中文，或完全使用中文
3. **描述清晰**: 文件名应准确反映内容

**正确示例**:
```
✓ 获取_user_access_token.md
✓ 创建文档.md
✓ 批量更新条件格式.md
```

**错误示例**:
```
✗ 获取 user access token.md  (包含空格)
✗ get-token.md               (使用英文)
✗ doc1.md                    (不清晰)
```

### 文档格式规范 (Document Format Standards)

每个文档应遵循以下结构：

```markdown
# 文档标题

最后更新于 YYYY-MM-DD

## 功能描述

简要说明该 API 的用途和主要功能。

## 基础概念

解释相关的术语和数据结构（如适用）。

## 使用限制

- 调用频率限制
- 数据大小限制
- 权限要求

## 请求参数

详细说明所有请求参数，包括：
- 参数名称
- 是否必填
- 数据类型
- 参数说明
- 示例值

## 响应格式

说明返回数据的结构和字段含义。

## 错误处理

列出常见错误码和处理方法。

## 示例代码

提供实际的 API 调用示例。
```

### Markdown 格式要求 (Markdown Format Requirements)

1. **标题层级**:
   - 每个文档必须以一级标题 `#` 开始
   - 使用正确的标题层级（H1 → H2 → H3）
   - 不要跳过层级

2. **代码块**:
   ```markdown
   ```json
   {
     "key": "value"
   }
   \```
   ```
   - 为代码块指定语言（json, bash, python 等）
   - 保持代码格式整洁

3. **列表**:
   - 无序列表使用 `*` 或 `-`
   - 有序列表使用 `1.`, `2.` 等
   - 保持缩进一致

4. **链接**:
   - 内部链接使用相对路径
   - 外部链接确保有效性
   - 使用描述性的链接文本

### 更新日期格式 (Update Date Format)

所有文档应在标题后包含更新日期：

```markdown
# 文档标题

最后更新于 2026-01-31
```

- 使用 `YYYY-MM-DD` 格式
- 每次实质性修改都应更新日期
- 仅更新从官方抓取时保留的原始日期

---

## 🔄 提交流程 (Submission Process)

### 1. Fork 项目
点击项目页面右上角的 "Fork" 按钮，创建您自己的副本。

### 2. 克隆到本地
```bash
git clone https://github.com/YOUR_USERNAME/Feishu_OpenAPI_DOC.git
cd Feishu_OpenAPI_DOC
```

### 3. 创建分支
```bash
git checkout -b feature/your-feature-name
# 或
git checkout -b fix/your-fix-name
```

### 4. 进行修改
- 遵循上述文档规范
- 一次只关注一个问题或功能
- 保持修改的最小化和针对性

### 5. 测试验证
在提交前，请检查：
- [ ] 文件名符合命名规范
- [ ] 文档包含正确的 H1 标题
- [ ] Markdown 格式正确
- [ ] 链接有效
- [ ] 代码示例可用
- [ ] 更新日期准确

### 6. 提交更改
```bash
git add .
git commit -m "描述您的更改"
```

**提交信息规范**:
- 使用清晰、描述性的提交信息
- 中文或英文均可
- 说明修改的内容和原因

**示例**:
```
✓ 修复 README 中的错误引用
✓ 更新电子表格 API 文档
✓ 添加缺失的 H1 标题
✓ Fix broken links in authentication docs
```

### 7. 推送到 GitHub
```bash
git push origin feature/your-feature-name
```

### 8. 创建 Pull Request
1. 访问您的 Fork 页面
2. 点击 "Pull Request" 按钮
3. 填写 PR 标题和描述
4. 说明您的更改内容和目的
5. 提交 PR 等待审核

---

## ✅ Pull Request 检查清单 (PR Checklist)

在提交 PR 前，请确认：

- [ ] 我已阅读并遵循贡献指南
- [ ] 文档格式符合项目规范
- [ ] 文件名遵循命名约定
- [ ] 所有文档都有正确的 H1 标题
- [ ] 更新日期已正确设置
- [ ] 链接已验证有效
- [ ] 代码示例已测试（如适用）
- [ ] 提交信息清晰明确
- [ ] 已解决合并冲突（如有）

---

## 🤝 行为准则 (Code of Conduct)

### 我们的承诺
我们致力于为每个人提供友好、安全和包容的环境。

### 我们的标准
**正面行为包括**:
- 使用欢迎和包容的语言
- 尊重不同的观点和经验
- 优雅地接受建设性批评
- 关注对社区最有利的事情
- 对其他社区成员表现出同理心

**不可接受的行为包括**:
- 使用性化的语言或图像
- 人身攻击或侮辱性评论
- 公开或私下骚扰
- 未经许可发布他人的私人信息
- 其他不道德或不专业的行为

---

## 📧 联系方式 (Contact)

如果您有任何问题或建议，请通过以下方式联系：

- **提交 Issue**: [GitHub Issues](https://github.com/BlueSkyXN/Feishu_OpenAPI_DOC/issues)
- **Pull Request**: [GitHub PRs](https://github.com/BlueSkyXN/Feishu_OpenAPI_DOC/pulls)

---

## 📜 许可证 (License)

通过向本项目贡献，您同意您的贡献将在 [GPL v3 许可证](LICENSE) 下授权。

---

## 🙏 致谢 (Acknowledgments)

感谢所有为本项目做出贡献的开发者和用户！

您的每一个贡献都让这个项目变得更好！

---

**最后更新**: 2026-01-31  
**维护者**: [@BlueSkyXN](https://github.com/BlueSkyXN)
