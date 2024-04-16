# 基础作业
## 配置 LMDeploy 运行环境
环境配置成功，直接上运行测试截图：
![alt text](home_work_image/lesson5/直接运行模型.png)

## 以命令行方式与 InternLM2-Chat-1.8B 模型对话
![alt text](home_work_image/lesson5/与LMDeploy部署的InterLM进行对话.png)

# 进阶作业
## 设置KV Cache最大占用比例为0.4，开启W4A16量化，以命令行方式与模型对话。（优秀学员必做）
启动KV Cache只需要加上参数：`--cache-max-entry-count 0.4`。  
1. 只设置KV Cache最大占用比例为0.4：
```bash
lmdeploy chat /root/internlm2-chat-1_8b --cache-max-entry-count 0.4
```
2. 进行W4A16量化之后，得到新的模型文件：
![alt text](home_work_image/lesson5/量化后的模型文件.png)
3. 内存占用比较：

**未KV Cache（默认0.8），未W4A16量化**
![alt text](home_work_image/lesson5/不量化的显存咱用.png)
**KV Cache = 0.4，未W4A16量化**
![alt text](home_work_image/lesson5/cache=0.4和不量化.png)
**KV Cache = 0.4，W4A16量化**
![alt text](home_work_image/lesson5/cache=0_4和量化.png)

## 以API Server方式启动 lmdeploy，开启 W4A16量化，调整KV Cache的占用比例为0.4，分别使用命令行客户端与Gradio网页客户端与模型对话。（优秀学员）
## 使用W4A16量化，调整KV Cache的占用比例为0.4，使用Python代码集成的方式运行internlm2-chat-1.8b模型。（优秀学员必做）
## 使用 LMDeploy 运行视觉多模态大模型 llava gradio demo （优秀学员必做）
## 将 LMDeploy Web Demo 部署到 [OpenXLab](../tools/openxlab-deploy/) （OpenXLab cuda 12.2 的镜像还没有 ready，可先跳过，一周之后再来做）