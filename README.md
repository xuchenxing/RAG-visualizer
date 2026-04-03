the introduction of this RAG visualization tool

https://www.youtube.com/watch?v=FqCftpE-5O8&t=27s

https://www.bilibili.com/video/BV16SwvzXEKx/

V2.0 版本更新
# 文档导入
## 新增段落分割策略，现支持5种分块方式（固定大小 / 段落分割 / 语义分块 / 句子分割 / 递归字符分割）
## 新增五策略并排对比图，同一段故宫原文在不同策略下的切割位置一目了然，点击卡片可直接切换当前策略
## 修复策略切换后 chunk 列表内容不变的问题，每种策略现有独立的真实文本，平均字数等指标实时更新
## 新增 Overlap 重叠区可视化，用颜色高亮相邻两个 chunk 共享的字符，直观解释重叠的意义

# 向量 Embedding
## 新增维度语义探索模块，10个可点击的维度格，展示该维度捕获的语义含义与相关 chunk
## 将"自定义文本输入框"改为语义聚类预设按钮（13个），按建筑结构 / 历史沿革 / 文物收藏 / 宫殿典礼 / 无关内容分组，点击后在向量空间中显示落点并可累积对比

# 向量索引
## 三种索引算法（HNSW / Flat / IVF）全部换成实时动画：HNSW 展示逐层跳跃的搜索路径，Flat 展示向量被逐一遍历的计数过程，IVF 展示查询飞向最近聚类中心的动画，并新增"▶ 重放"按钮
## 新增三张算法对比卡片，展示各算法的工作原理、搜索复杂度、召回率和最适场景，点击可切换
## 新增向量数据库选型决策树，根据数据规模 → 部署偏好 → 运维能力 → 技术栈，交互式推荐方案（7个数据库），附理由与权衡点

# 语义检索
## 检索策略默认改为"语义 + 重排序"
## 新增两阶段检索可视化：左侧展示 Top-20 粗召回候选，右侧展示 Cross-encoder 精排后的 Top-5，每条结果标注排名升降箭头（↑3 / ↓1 / —）
## 新增混合检索三栏对比：BM25 关键词排名、向量语义排名、RRF 融合结果三列并排，标注各 chunk 在两路中的原始排名
## 新增 min_score 阈值滑块，实时过滤检索结果，阈值过高时出现红色警告
## 新增精准 vs 模糊查询对比，展示同一知识库下不同查询措辞的得分差异

# 增强生成
## 新增有 RAG vs 无 RAG 输出对比，纯 LLM 的错误数字用红色底色高亮，RAG 增强后的精确数据用绿色标出并附来源引用
## 新增常见错误模式诊断，4张卡片覆盖 Chunk 过大 / Chunk 过小 / 嵌入模型弱 / 知识库缺失，每张展示现象、得分示意、根因与修复建议

# 全局
## 新增**▶ 自动演示**按钮，每3.5秒自动切换一个阶段，底部弹出进度条与状态文字
## 新增全面入场动画：Token 色块弹跳出现、向量柱从零生长、检索结果从左侧依次划入、最终答案逐字打字机输出
## 五个面板全部重构为STEP 流程结构，顶部为数据流总览（INPUT → OUTPUT），下方各 STEP 对应具体操作环节

<img width="2560" height="1272" alt="2b7191e516d2ba922941bac3a69fa2d4" src="https://github.com/user-attachments/assets/aa4c8e4f-631b-47ff-9104-8a9845ffa30c" />

<img width="3234" height="1520" alt="image" src="https://github.com/user-attachments/assets/ee4bce4b-3d6e-478b-be03-9993b8462e8e" />

<img width="3218" height="1732" alt="image" src="https://github.com/user-attachments/assets/32dd1ef5-8219-4ad2-840b-17b614b7a3d1" />

<img width="2976" height="1832" alt="image" src="https://github.com/user-attachments/assets/e1cc50d7-5f37-4e22-8f89-cfba3491827d" />




