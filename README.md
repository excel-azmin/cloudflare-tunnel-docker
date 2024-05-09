# cloudflare-tunnel-docker

version: '3'

services:
  cloudflared_tunnel:
    image: cloudflare/cloudflared:latest
    command: tunnel --no-autoupdate run --token your token
    restart: unless-stopped
    networks:
      - cloudflared_network

networks:
  cloudflared_network:
    
