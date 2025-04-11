# ISP个人实验报告 - 22人工智能

本项目为笔者在厦门大学人工智能系2024年小学期电子工艺实训课程上完成的成果

## 项目简介

本项目是一次关于人工智能应用的综合实验，涵盖了环境配置、端边云协同以及手写数字识别三大核心部分。通过本次实验，我们深入了解了云计算、边缘计算和本地计算的协同工作模式，并在华为云的ModelArts平台上进行了AI模型的训练和部署。此外，我们还利用MindSpore框架在本地进行了手写数字识别模型的训练。

## 技术栈

- **操作系统**：Windows 11, Ubuntu (WSL2)
- **开发平台**：华为云的ModelArts
- **深度学习框架**：MindSpore
- **环境管理工具**：Anaconda
- **代码编辑器**：VS Code

## 实验流程

### 1. 环境配置

#### Windows 11 & WSL2
- **安装Hyper-V**：在Windows 11家庭版中手动安装Hyper-V。
- **启用WSL2**：通过控制面板启用Windows虚拟化和Linux子系统（WSL2）。
- **安装Ubuntu**：通过命令行安装最新版本的Ubuntu。
- **子系统换盘**：将Ubuntu子系统移动到非系统盘以节省空间。

#### Anaconda安装
- **更新apt-get**：确保包管理工具最新。
- **安装SSH和wget**：便于文件传输和下载。
- **下载并安装Anaconda**：通过wget下载Anaconda安装包并进行安装。

#### VS Code远程连接
- **安装插件**：在VS Code中安装相关插件以支持远程开发。
- **创建conda环境**：在Ubuntu子系统中创建Python虚拟环境。

### 2. 端边云协同

#### 准备工作
- **注册并认证华为云账号**。
- **创建OBS桶**：用于存储数据集和模型。
- **购买ECS云服务器**：根据需要选择CPU型或GPU加速型。
- **配置安全组和弹性公网IP**。

#### 自动学习基础
- **口罩检测项目**：创建项目、运行数据标注、运行工作流、进行预测分析并清除资源。
- **垃圾分类项目**：仿照口罩检测项目的流程进行操作。

#### 开发环境实践
- **创建NoteBook实例**：在ModelArts上创建NoteBook实例进行代码编写和实验记录。
- **尝试使用Codelab**：利用免费算力进行模型训练。
- **VS Code插件安装与连接**：安装VS Code插件并连接到ModelArts的开发环境。

#### ModelArts Standard自定义算法
- **准备代码文件**：包括train.py, customize_service.py, config.json等。
- **上传文件与数据**：到OBS桶中。
- **创建训练作业**：在ModelArts上创建自定义算法的训练作业。
- **部署在线服务**：将训练好的模型部署为在线服务并进行预测。

### 3. 手写数字识别

#### 下载MindSpore
- 在Windows和Ubuntu上分别下载并安装MindSpore框架。

#### 代码准备与运行
- **获取代码**：从MindSpore官网获取手写数字识别的示例代码。
- **运行训练代码**：在本地虚拟环境中运行训练代码并生成模型文件。

## 成果展示

- **环境配置成功**：WSL2、Anaconda和VS Code远程连接均配置成功。
- **端边云协同成果**：口罩检测和垃圾分类模型成功部署并进行预测。
- **自定义算法训练与部署**：成功训练出手写数字识别模型并部署为在线服务。
- **本地训练成果**：在本地利用MindSpore框架训练出手写数字识别模型。


## 许可证

本项目采用[MIT许可证](https://opensource.org/licenses/MIT)。

## 贡献指南

欢迎任何形式的贡献！如果您发现了问题或想要改进项目，请按照以下步骤操作：

1. Fork本仓库
2. 创建新的分支 (`git checkout -b feature/your-feature-name`)
3. 提交更改 (`git commit -am 'Add some feature'`) 
4. 推送分支到您的远程仓库 (`git push origin feature/your-feature-name`)
5. 打开一个Pull Request

感谢您的贡献！
