# 基础作业
## 使用 InternLM2-Chat-1.8B 模型生成 300 字的小故事（需截图）
![alt text](home_work_image\lesson2\1.png)

# 进阶作业
## 熟悉 huggingface 下载功能，使用 huggingface_hub python 包，下载 InternLM2-Chat-7B 的 config.json 文件到本地（需截图下载过程）
链接：https://huggingface.co/docs/hub/models-adding-libraries#download-files-from-the-hub  

新建一个文件`download_config.py`，输入：
```python
from huggingface_hub import hf_hub_download
hf_hub_download(repo_id="internlm/internlm2-chat-7b", filename="config.json", local_dir="/root/demo")
```
注意，repo_id和filename都需要从Huggingface上确认。终端运行之后，得到：
![alt text](home_work_image\lesson2\2.png)

## 完成 浦语·灵笔2 的 图文创作 及 视觉问答 部署（需截图）


