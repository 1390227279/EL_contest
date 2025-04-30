# Preparation
## 1.确保Linux环境：

如果使用Windows电脑：必须按照要求启用WSL，并安装Ubuntu 22.04。所有开发工作都要在这个WSL/Ubuntu环境里进行。 （如果你不熟悉WSL，可以把它想象成在Windows里开了一个小窗口，里面运行着一个纯净的Linux系统，专门用来写代码）。

如果使用Mac或Linux电脑：可以直接使用自带的终端。

## 2.安装Python环境管理器 (Conda)：

所有人都需要安装Conda（推荐Miniconda）。

创建独立的虚拟环境：为这个项目创建一个专门的conda虚拟环境（例如 conda create -n text_detector python=3.9），然后激活这个环境（conda activate text_detector）。之后所有的Python包（依赖）都必须安装在这个虚拟环境里，不能装在系统默认环境里。这能避免不同项目间的库冲突。

## 3.安装代码编辑器：安装VSCode或Cursor，这些编辑器对在Linux环境和远程开发支持较好。

## 4.安装版本控制工具 (Git)：所有人都需要安装Git。