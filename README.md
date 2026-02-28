# Poem-Vision （面向视觉意境的诗词检索与生成）  
一个多模态人工智能系统，融合计算机视觉、语义向量与诗词生成技术，能够理解图像中的视觉意境，检索与之匹配的古典诗词，并基于画面意境生成新的诗句。  
## 一、预计目标产出：
| 模块 | 具体产出 |
|------|----------|
| 数据集 | 标注意境的图像库 + 诗词向量库 |
| 模型 | 意境分类器、图文检索模型、诗词生成器 |
| 后端 | API服务、向量检索引擎 |
| 前端 | 交互界面（H5/小程序/Web） |
| 论文/报告 | 技术方案 + 实验结果分析 |
| Demo视频 | 系统演示，展示典型用例 |
## 二、项目文件夹规划：
Poem-Vision/
├── README.md                 # 项目介绍、快速开始、一月交付计划
├── LICENSE                   # 开源许可证
├── .gitignore                # Git 忽略文件（Python、IDE、模型文件等）
├── requirements.txt          # 项目依赖（PyTorch, transformers, fastapi 等）
├── setup.py                  # 可选：安装脚本
│
├── docs/                     # 文档
│   ├── architecture.md       # 系统架构设计
│   ├── api_spec.md           # API 接口文档
│   └── demo.md               # 使用演示说明
│
├── data/                     # 数据管理
│   ├── raw/                  # 原始数据：图像、诗词文本
│   ├── processed/            # 处理后数据：特征向量、索引文件
│   └── scripts/              # 数据处理脚本（下载、清洗、向量化）
│
├── models/                   # 模型定义与训练
│   ├──意境分类器/              # 子模块：图像意境分类
│   │   ├── model.py
│   │   └── train.py
│   ├──图文检索/                # 子模块：跨模态检索
│   │   ├── model.py
│   │   └── train.py
│   └──诗词生成/                # 子模块：意境到诗句生成
│       ├── model.py
│       └── train.py
│
├── backend/                  # 后端服务
│   ├── api/                  # API 路由与逻辑
│   │   ├── __init__.py
│   │   ├── routes.py         # 端点定义
│   │   └── utils.py          # 辅助函数
│   ├── vector_engine/        # 向量检索引擎（FAISS/Annoy）
│   │   └── searcher.py
│   └── app.py                # 主应用入口（FastAPI/Flask）
│
├── frontend/                 # 前端界面
│   ├── static/               # CSS、JavaScript、图片
│   ├── templates/            # HTML 模板
│   └── app.py                # 简单前端服务（可选）
│
├── notebooks/                # Jupyter 实验与分析
│   ├── 01_意境分类探索.ipynb
│   ├── 02_检索模型评估.ipynb
│   └── 03_生成样例展示.ipynb
│
├── tests/                    # 单元测试
│   ├── test_models.py
│   └── test_api.py
│
├── scripts/                  # 实用脚本
│   ├── build_vector_db.py    # 构建诗词向量库
│   ├── evaluate.py           # 模型评估
│   └── demo_run.py           # 本地快速演示
│
└── results/                  # 训练结果与输出
    ├── figures/              # 图表（损失曲线、示例图）
    └── logs/                 # 训练日志
