## 画册功能的使用方法：
你需要安装 node.js然后执行以下步骤：
1. 在 hugo.toml 中管理分类：
```
[params.gallery]
  categories = [
    { id = "scenery", name = "风景" },
    { id = "life", name = "生活" },
    # 添加新分类就在这里加一行
    { id = "new-category", name = "新分类" }
  ]
```
2. 图片文件命名时使用配置中定义的 id
- 前三部分必须是日期：YYYY-MM-DD        
- 第四部分是分类名：必须与模板中的id值完全匹配
- 最后部分是图片标题：可以自由命名

```
2024-01-01-scenery-mountain.jpg  # id="scenery"
2024-01-02-life-party.jpg       # id="life"
2024-01-03-food-cake.jpg        # id="food"
2024-01-04-travel-paris.jpg     # id="travel"
2024-01-05-pet-cat.jpg          # id="pet"
2024-01-06-other-misc.jpg       # id="other"
```
3. 在博客根目录下执行 `hugo generate-images` 命令，生成图片的相对路径
```
D:\>node D:\blog\themes\simple\static\js\generate-images.js
图片数据已生成: D:\blog\themes\simple\static\data\images.json
共处理 2 张图片

分类统计:
scenery: 2张
```