# 系统工程入门实践(TP)指南：使用SysML和Visual Paradigm

---

这份文档是 `TP-INS-2021-22-v1.pdf` 的中文翻译和总结，旨在帮助您理解实践任务的要求。

## 概述

Visual Paradigm 是一款功能非常全面的建模软件，支持UML, SysML, BPMN等多种建模语言，广泛用于软件和系统设计。完成本次TP需要使用INSA许可的Visual Paradigm软件。

**注意：** 如果您使用最新版本的软件编辑文件，可能会无法在旧版本中打开。

本次TP旨在让您初步掌握系统工程的基本方法，这些技能在未来的项目（如集体项目、自动化项目）中将会非常有用。

### **最终需要提交的产物**

您需要在实践课程结束时提交一份**个人报告（PDF格式）**。

这份报告需要和您的 **Visual Paradigm项目文件（.vpp）** 一起打包成一个 **ZIP文件**，然后上传到Moodle平台。

报告中应包含对图表的补充说明，您也需要在课程期间随时撰写这份报告，简要解释和证明您的设计思路。

---

## 1. 前提条件

在开始实践课程之前，您的计算机上需要已经安装好 **Visual Paradigm 16.3版本**。

---

## 2. 打开项目

1.  启动 Visual Paradigm 软件。
2.  为了避免从零开始，课程已经在Moodle上提供了一个包含基础图表和模型结构的项目文件。请下载该文件并在VP软件中打开它（通过菜单 "Project" -> "Open"）。
3.  **请务必经常保存您的项目！** 因为最终需要提交这个文件。

---

## 3. 分析需求规格说明书 (Cahier des Charges)

### 3.1 需求规格说明书

请从Moodle下载名为“Cahier des Charges”的文件。这份文件是2019-20年度的考题，是您本次建模工作的主要依据。
*(注：根据我们之前的分析，这份文件并不是一个单独的文档，您需要从 `5GE1.pdf`, `5GE2.pdf`, `5GE3.pdf` 这些文件中提炼需求)。*

### 3.2 模型的组织结构

在TP中添加模型元素（如活动、模块、需求、参与者等）时，请务必**复用**在其他图表中已经创建过的元素，而不是创建重名的“克隆体”。

为了做到这一点，您可以通过顶部菜单 "View" -> "Project Browser"，然后在 "Model Structure" 中找到已经存在的元素，将它们拖拽到您当前的图表中使用。

### 3.3 需要完成的内容

您的核心任务是**补全**项目文件中的图表和模型，以分析需求规格说明书。

#### 3.3.1 环境与参与者 (Environnement et acteurs)

*   **添加模块 (Block):** 将 "Block" 元素从工具栏拖拽到图中。
*   **更改构造型 (Stereotype):** 选中一个模块，点击键盘 "Enter" 键，在弹出的窗口中选择 "Stereotypes" 选项卡进行修改（例如，从 `<<block>>` 修改为 `<<system>>`）。

#### 3.3.2 当前与期望流程 (Process actuel et désiré)

*   修改并添加新的**活动图 (Activity Diagram)**，并使用**控制流 (Control Flow)**来表示当前和期望的业务流程。
*   *提示: 可以使用垂直泳道（Vertical Swimlane）工具来划分不同角色的活动。*

#### 3.3.3 预期使用场景 (Scenarios d'usage attendu)

*   创建一个**网格图 (Grid Diagram)** 来自动生成用例（Use Case）列表。
*   创建方法：菜单 "Diagram" -> "New" -> "Grid" (在 "Others" 类别下)。
*   选择模型元素为 "Use Case"，并配置您想在表格中显示的列，如ID、名称、描述和主要参与者。

#### 3.3.4 信息流 (Flux d'informations)

*   补全 **IBD图 (Internal Block Diagram)**，该图位于 `3.3 Flux d'information désirés` 子模型下。
*   **复用模块:** 从左侧的 "Model Explorer" 中找到之前创建的模块，拖入图中。
*   **添加端口 (Port):** 使用 "Port" 工具在模块上添加输入/输出端口。
*   **连接端口:** 使用 "Connector" 工具连接端口。

#### 3.3.5 需求 (Exigences)

*   补全 **REQ图 (Requirement Diagram)**，该图位于 `4 Exigences` 子模型下。
*   **分解需求:** 将主要需求分解为多个子功能需求。
*   **关联需求:** 将与用户交互相关的需求和对应的用例（Use Case）连接起来（使用 "refine" 关系）。
*   **区分需求类型:** 使用不同的构造型（如 "performance"）来区分约束性需求和其他需求。

### 3.4 建立初步的可追溯性 (Traçabilité)

*   使用 **矩阵图 (Matrix Diagram)** 来验证所有的用例都与至少一个需求相关联。
*   矩阵的行（Rows）和列（Columns）可以分别设为用例和需求。
*   通过显示 "by Relationship" 类型的关联，可以自动展示用例和需求之间的 "refine" 关系。
*   **检查并确保所有用例都已关联到相应的接口需求。**

---

## 4. 结束

1.  保存您的Visual Paradigm项目文件 (`.vpp`)。
2.  将项目文件和您撰写的PDF报告压缩成一个 **ZIP** 文件。
3.  将ZIP文件上传到Moodle。

---

## 5. 补充信息

### 5.1 创建报告和演示

*   您可以使用 "Tools" -> "Doc" -> "Build Doc from Scratch" 功能，从您的模型直接生成报告。

### 5.2 协同工作

*   Visual Paradigm 支持多人协同工作（类似Git）。

### 5.3 其他有用的工具

*   **RACI矩阵:** 在 "Modeling" -> "Impact Analysis" -> "Chart" 中可以创建RACI责任分配矩阵。
*   **版本比较:** 在 "Modeling" -> "Visual Diff" 中可以比较两个`.vpp`文件的差异。
