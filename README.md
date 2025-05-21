# 静态HTML页面Docker部署

这个项目使用Docker和Nginx来部署Siliconflow Token静态HTML页面。

## 文件结构

- `index.html` - 静态HTML页面
- `Dockerfile` - 用于构建Docker镜像的配置文件
- `docker-compose.yml` - 用于简化Docker部署的配置文件

## 部署说明

### 方法一：使用Docker run（推荐）
  ```bash
docker run -d -p 8080:80 omentwwnmfm/siliconflow-token:latest
   ```
### 方法二：使用Docker命令
1. 首先使用git命令
   ```bash
   git clone https://github.com/OmenTwwnmfm/Siliconflow-Token.git
   ```
1. 构建Docker镜像
   ```bash
   docker build -t siliconflow-token .
   ```

2. 运行Docker容器
   ```bash
   docker run -d -p 8080:80 siliconflow-token
   ```

### 方法三：使用Docker Compose

1. 启动服务
   ```bash
   docker-compose up -d
   ```

2. 停止服务
   ```bash
   docker-compose down
   ```

## 访问网站

部署完成后，可以通过浏览器访问：

```
http://localhost:8080
```

## 注意事项

- 使用Docker Compose部署时，已配置卷挂载，可以直接修改本地HTML文件，无需重新构建镜像
- 默认端口为8080，如需修改，请在docker-compose.yml文件中更改ports配置
