# JellyGo! 家庭全能自驾助手
基于 OpenAgents 构建的多智能体协作网络，为带娃家庭+新能源车用户提供自驾全流程定制服务。


## 项目概述
- **Network ID**：jellygo-family-drive-assistant
- **一句话简介**：通过8个AI Agent协同，一键生成「带娃+新能源车」场景下的自驾行程、预算、补能、安全全方案
- **目标用户**：亲子家庭自驾用户、新能源车长途自驾用户
- **核心场景**：家庭自驾前全方案规划、自驾中动态行程/补能调整


## 技术架构
- **依赖工具**
  - OpenAgents 版本：v0.2.0
  - 技术栈：Python 3.9+、OpenAgents SDK、大语言模型（GPT-4.1）
- **Agent Network 设计思路**
  采用「主Agent统筹+专项Agent分工」模式：以 `RoadTripMainAgent` 为核心调度中枢，调用8个专项Agent完成需求解析、规划、核算等工作，各Agent通过OpenAgents网络实现自主协作与冲突协调。
- **核心流程**
  用户需求输入 → Charlie解析信息 → 主Agent启动专项Agent → 各Agent自主沟通调整 → 输出全流程方案


## 核心Agent分工
| Agent名称               | 功能定位                     |
|-------------------------|------------------------------|
| RoadTripMainAgent       | 核心调度中枢，整合全流程方案 |
| Charlie                 | 需求信息解析与提取           |
| Budget-calculator-agent | 自驾预算核算与政策适配       |
| Route-planner-agent     | 亲子友好型行程规划           |
| Charging-station-agent  | 新能源车补能方案适配         |
| Critic                  | 儿童安全项目筛选与管控       |
| Weather-agent           | 自驾天气预警与行程调整       |
| Assistant               | 自驾装备与生活细节提醒       |


## 如何使用
1. 克隆本仓库：
   ```bash
   git clone https://github.com/jellypp2025/jellygo-family-drive-assistant.git

