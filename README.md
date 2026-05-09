# simplyit-ai-backend-infra

## Launch Sequence

### 1 - NPM
- Compose launch
- Add Cloudflare DNS-Challenge API Key
- Setup wildcard SSL through Cloudflare DNS-Challenge 

### 2 - Portainer
- Compose launch
- Connect to NPM

### 3 - N8N | bundle: mongo, mongo-express, qdrant
- Compose launch
- Connect to NPM: n8n, mongo-express, qdrant
  - Set basic auth for mongo-express & qdrant, and disable when not in use. 


#### Port configurations
- NPM
  - Port 81 - self reverse proxy
- Portainer
  - Port 9000 - ngnix reverse proxy
- N8N
  - Port 5678 - ngnix reverse proxy
- MongoDB
  - Port 27017 - internal only
- Mongo Express
  - Port 8081 - ngnix reverse proxy
- Qdrant
  - Port 6333 - internal only
