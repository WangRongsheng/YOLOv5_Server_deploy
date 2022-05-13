# 简介

YOLOv5的服务端部署方案，可以提供本地或者云端API服务。

> 注意，核心代码已加密（不可反编译，不要费力气了！）

# 使用

1. 克隆下载本仓库代码
2. 修改必要配置为文件，创建修改`config.yaml`：
```html
HOST: ip address
PORT: 端口

FOLDER: ['caches', 'results','results_json']
CACHE_FOLDER: caches
RESULTS_FOLDER: results
ALLOWED_EXTENSIONS: ['png', 'jpg', 'jpeg']

MYDEVICE: 设备（cpu还是cuda）
IMG_SIZE: 640
THRESHOLD: 模型置信度
DIR_PATH: Serving_model/commodity/
```
3. 把官方或者自己训练的模型权重(.pt)放在`Serving_model/commodity/1`文件夹下，同时保证你放入的模型命名必须为：**best.pt**
4. `python server.py`稍等片刻
5. 打开`ip:port`，如：`127.0.0.1:8090`

# 完整代码

[https://mianbaoduo.com/o/bread/Ypiamphy](https://mianbaoduo.com/o/bread/Ypiamphy)