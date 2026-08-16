FROM node:22-slim

# Install networking dependencies for internet connectivity
RUN apt-get update && apt-get install -y git curl ca-certificates && rm -rf /var/lib/apt/lists/*

# Install Claude
RUN npm install -g @anthropic-ai/claude-code

# Create non-root user
RUN useradd -m -u 1000 ai-user
USER ai-user

WORKDIR /workspace
ENTRYPOINT ["claude"]
