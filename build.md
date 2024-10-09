docker buildx create --use

docker buildx build --platform linux/arm64,linux/amd64 -t yinqf7437/duckduckgo-api:1.2.0 . --push

docker buildx build --platform linux/amd64 -t yinqf7437/duckduckgo-api:1.2.0 . --push

docker run -d -p 8000:8000 yinqf7437/duckduckgo-api:1.2.0
