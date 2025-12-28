# GitHub 数学公式显示说明

## 问题说明

如果你在 GitHub 上看到的数学公式显示为原始代码（如 `$s_t$`）而不是渲染后的数学符号，这不是浏览器插件的问题，而是 GitHub 的数学公式渲染限制。

## GitHub 数学公式支持情况

### ✅ 支持的位置
1. **README.md 文件** - 完全支持
2. **Issues 和 Pull Requests** - 支持
3. **Wiki 页面** - 支持
4. **Gist** - 支持

### ⚠️ 限制
- **普通 .md 文件**：GitHub 在某些情况下可能不会自动渲染数学公式
- **Raw 文件视图**：永远不会渲染，只显示原始代码

## 解决方案

### 方案1：在 README.md 中查看（推荐）

创建一个 README.md 文件，链接到 papers.md：

```markdown
# arXiv 论文分析结果

查看完整的论文分析：[papers.md](github_output/papers.md)
```

然后在 README.md 中直接显示一些示例公式，确认渲染是否正常。

### 方案2：使用 GitHub Pages

1. 启用 GitHub Pages
2. 使用支持 MathJax 的 Markdown 渲染器（如 Jekyll + MathJax）

### 方案3：使用在线 Markdown 查看器

以下工具支持数学公式渲染：

1. **Typora**（桌面应用）
2. **Mark Text**（桌面应用）
3. **在线工具**：
   - https://dillinger.io/
   - https://stackedit.io/
   - https://markdown.xyz/

### 方案4：本地查看（推荐用于阅读）

使用支持数学公式的 Markdown 编辑器：

1. **Typora** - 完全支持 LaTeX 数学公式
2. **Mark Text** - 开源，支持数学公式
3. **VS Code** - 安装 "Markdown Preview Enhanced" 插件

## 验证公式格式

公式格式应该是：

- **行内公式**：`$x = 1$`（注意前后有空格）
- **块级公式**：
  ```
  $$
  x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
  $$
  ```

## 测试公式渲染

访问以下链接测试 GitHub 的数学公式渲染：

1. 你的仓库 README（如果存在）
2. 创建一个测试 Issue，输入：`这是测试公式 $E=mc^2$`

如果 Issue 中的公式能正确渲染，说明 GitHub 支持数学公式，但可能在普通 .md 文件中有限制。

## 当前状态

你的 `papers.md` 文件中的公式格式是正确的，例如：
- `$ X_{1:t} = \{I, C, A, J\}_{1:t} $`
- `$ \mathbf{p}_i = (x_i, y_i, z_i) $`

这些公式在支持 MathJax 的环境中应该能正确渲染。

## 建议

**最佳实践**：使用支持数学公式的本地 Markdown 编辑器（如 Typora）来阅读 `papers.md` 文件，这样可以获得最佳的阅读体验。

