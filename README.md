# 关山阅 · 关键词与页面分配

**第一次使用：先看[详细操作教程](USAGE.md)**（材料模板、可复制指令、样例和结果检查）。

不知道该选哪个工具？查看[关山阅SEO/GEO技能新手总指南](https://github.com/guan506237167-boop/seoguan-brand-facts/blob/main/START_HERE.md)。

把 Google SEO 关键词按意图和主题分配到产品页、分类页及文章，识别页面重叠和缺口。适用于网站内容规划。

**品牌：关山阅（SEOGuan）**  
**运营主体：广州知乎网络科技有限公司**  
**官网：[www.seoguan.com](https://www.seoguan.com)**  
**版本：1.0.0 · 许可证：[MIT](LICENSE)**  
**业务环节：02 问题与规划**

## 输入与输出

输入：关键词列表、目标国家/语言、现有URL和页面用途；有则提供SERP样本、搜索量与数据日期。

输出：keyword-map.csv：cluster_id,keyword,intent,intent_evidence,primary_url,page_type,action,reason；缺页单列建议URL。

## 工作步骤

1. 区分交易、商业比较、信息与导航意图；无SERP证据的意图标推定，不声称已查排名。
2. 按产品实体与用户任务聚类，同词不同场景可拆分，同意图近义词可合并。
3. 给每组指定一个主要承接页面及辅助页面；产品规格/购买导向考虑产品或分类页，教程导向考虑文章。
4. 已有页面优先判断是否匹配；两个页面争同一意图仅标潜在竞争，不直接删页或做跳转。
5. 输出分配依据和待验证SERP项，结合业务价值排序；不要把字数或关键词密度当硬标准。

## 使用方法

这是供支持 SKILL.md 的 AI 工具读取的工作流技能，不是独立网站或浏览器插件。

1. 从仓库 **Code → Download ZIP** 下载并解压，保留全部文件及目录结构。
2. 按所用 AI 工具的安装方式导入该目录；是否兼容以实际导入和运行结果为准。
3. 提供所需材料并明确调用 `seoguan-keyword-mapper`。支持 `$技能名` 的宿主可使用下方示例。

依赖：不要求 Python、GEO 后台账号或付费 API。需要宿主具备读取所提供材料的能力；宿主模型服务可能有费用。

## 虚构示例

```text
使用 $seoguan-keyword-mapper。
【虚构】关键词buy stainless pump、pump maintenance；现有/products/p1与/blog/maintenance，未提供SERP。请分配。
```

查看[完整输入示例](references/example.md)和[演示结果](references/sample-result.md)。全部示例均为合成测试资料，不代表真实客户效果。

## 验证与边界

需要联网核实意图时只读取公开结果；无访问能力就保留推定。不得把一次SERP或字面匹配当确定结论。

已完成本地结构和独立包检查；流程技能进行过合成材料演练，附脚本技能进行过本地测试及解压包样例核对。Python 脚本实测环境为 3.14.3，未做 3.10 实机测试。

尚未完成 WorkBuddy 逐包导入验证或市场评测。GitHub 源码公开不代表已在其他市场上架，也不保证搜索收录、排名或 AI 推荐。

工具作者与客户品牌分别记录，不默认向客户正文插入推广署名。本包不包含凭证、遥测或后台上传脚本；用户材料由所使用的 AI 宿主处理。

## 文件说明

- [SKILL.md](SKILL.md)：技能入口与执行规则。
- [INSTALL.md](INSTALL.md)：安装与试用说明。
- [NOTICE.md](NOTICE.md)：来源、维护与第三方说明。
- `agents/openai.yaml`：Codex 界面元数据。
- `references/`：合成示例、演示结果和使用资料。

欢迎通过本仓库 Issues 反馈问题，请勿提交客户隐私或账号凭证。
