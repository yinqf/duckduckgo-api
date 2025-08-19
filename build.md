docker buildx create --use

docker buildx build --platform linux/arm64,linux/amd64 -t registry.cn-hongkong.aliyuncs.com/yinqf/duckduckgo-api:1.3.0 . --push

docker buildx build --platform linux/amd64 -t registry.cn-hongkong.aliyuncs.com/yinqf/duckduckgo-api:1.3.0 . --push

docker run -d -p 8000:8000 registry.cn-hongkong.aliyuncs.com/yinqf/duckduckgo-api:1.3.0
