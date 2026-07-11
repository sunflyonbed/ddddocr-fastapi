# 使用官方 Python 运行时作为父镜像
FROM python:3.9-slim

ARG BUILD_VERSION=dev
ARG BUILD_ARCH=amd64

LABEL \
    io.hass.version="${BUILD_VERSION}" \
    io.hass.type="addon" \
    io.hass.arch="${BUILD_ARCH}" \
    org.opencontainers.image.title="DdddOcr FastAPI" \
    org.opencontainers.image.description="Home Assistant add-on for DdddOcr FastAPI"

# 设置工作目录
WORKDIR /app

# 将当前目录内容复制到容器的 /app 中
COPY . /app

# 安装项目依赖
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        libgl1 \
        libglib2.0-0 \
        libgomp1 \
    && pip install --no-cache-dir -r requirements.txt \
    && chmod a+x /app/run.sh \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# 暴露端口 8000
EXPOSE 8000

# 运行应用
CMD ["/app/run.sh"]
