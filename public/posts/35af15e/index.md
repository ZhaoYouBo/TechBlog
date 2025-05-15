# Label Studio


<!--more-->

## 安装

### 安装

```powershell
pip install label-studio
```

### 使用

```powershell
label-studio
```

## 自动化标注（YOLO）

### 克隆仓库

```powershell
git clone https://github.com/HumanSignal/label-studio-ml-backend.git
cd label-studio-ml-backend/examples/yolo
```

### 配置环境变量

- **`ALLOW_CUSTOM_MODEL_PATH=true`**：确保在 Docker 环境变量中设置此项，以允许 ML 后端加载自定义模型路径（`true`默认情况下）。
- **`LABEL_STUDIO_URL`**：必须指定 Label Studio 实例的外部 IP。如果您在本地运行 Label Studio 和 ML 后端，可以尝试将其设置为`LABEL_STUDIO_URL=http://host.docker.internal:8080`。
- **`LABEL_STUDIO_API_KEY`**：需要指定 Label Studio 实例的 API 密钥。

### 挂载自定义模型

```powershell
/app/models/<your-model>.pt
```

### 启动容器

```powershell
docker-compose up --build
```

### 配置标签

```xml
<View>
  <Image name="image" value="$image"/>
  <RectangleLabels name="label" toName="image" model_path="my_model.pt" model_score_threshold="0.25">
    <Label value="Car" background="blue" predicted_values="jeep,cab,limousine,truck"/>
  </RectangleLabels>
</View>
```

### 将 ML Backend 连接到 Label-Studio

1. 打开 Label Studio 实例。
2. 转到项目的**设置。**
3. 导航到**模型**选项卡。
4. 通过输入 ML 后端 URL 连接到 ML 后端。

```powershell
# 本地运行
http://localhost:9090
```

## 问题处理

### 网络连接问题

```powershell
failed to resolve source metadata for docker.io/pytorch/pytorch:2.1.2-cuda12.1-cudnn8-runtime
Get "https://auth.docker.io/token...": dial tcp ...:443: connectex: Connection timed out
```

可临时设置代理

```powershell
$env:HTTP_PROXY = "http://127.0.0.1:7897"
$env:HTTPS_PROXY = "http://127.0.0.1:7897"
```



---

> 作者: ZhaoRongBo  
> URL: http://localhost:1313/TechBlog/posts/35af15e/  

