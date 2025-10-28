FROM n8nio/n8n:latest
USER root

# Install ffmpeg and enhanced media processing tools + nodejs & npm for n8n community nodes
RUN apk add --no-cache \
    ffmpeg \
    imagemagick \
    exiftool \
    mediainfo \
    sox \
    ghostscript \
    python3 \
    py3-pip \
    nodejs \ 
    npm \
    && rm -rf /var/cache/apk/*

# Install n8n community nodes
RUN npm install -g \
    n8n-nodes-globals \
    n8n-nodes-text-manipulation \
    n8n-nodes-cronlytic \
    n8n-nodes-youtube-transcript-api \
    n8n-nodes-miniflux \
    n8n-nodes-neo4j || true
    # n8n-nodes-qdrant \
    # n8n-nodes-openrouter \
    # n8n-nodes-python \
    # n8n-nodes-perplexity \
    # n8n-nodes-searxng \
    # n8n-nodes-rss-feed-trigger \

# Install Python libraries for advanced media processing
RUN pip3 install --no-cache-dir --break-system-packages \
    pydub \
    Pillow \
    && rm -rf /root/.cache

# Create media directories with proper permissions for node user
# UID 1000 is the node user in the n8n container
RUN mkdir -p /data/media /data/temp && \
    chown -R 1000:1000 /data/media /data/temp && \
    chmod 775 /data/media /data/temp

USER node
WORKDIR /data
