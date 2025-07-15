# 🚀 Guia Rápido de Início

## ⚡ Configuração em 5 Minutos

### 1. Pré-requisitos
- Docker e Docker Compose instalados
- Git instalado

### 2. Clone e Configure
```bash
# Clone o projeto
git clone <url-do-repositorio>
cd n8n-queue

# Configure as variáveis de ambiente
cp evolution.env.example evolution.env
cp .env.example .env

# Edite os arquivos com suas senhas
nano .env
nano evolution.env
```

### 3. Inicie o Sistema
```bash
# Inicie todos os serviços
docker-compose up -d

# Verifique se está tudo funcionando
docker-compose ps
```

### 4. Acesse as Interfaces
- **.env**: `N8N_EDITOR_BASE_URL`
- **evolution.env**: `SERVER_URL`

## 🔧 Configurações Essenciais

### Senhas Obrigatórias (altere no .env)
```env
POSTGRES_PASSWORD=sua_senha_postgres
REDIS_PASSWORD=sua_senha_redis
N8N_BASIC_AUTH_PASSWORD=sua_senha_n8n
```

### Chave API Evolution (altere no evolution.env)
```env
AUTHENTICATION_API_KEY=sua_chave_api_evolution
```

## 🆘 Problemas Comuns

### Porta já em uso
```bash
# Verificar portas em uso
netstat -tulpn | grep :5678
netstat -tulpn | grep :8080

# Parar serviços conflitantes ou alterar portas no docker-compose.yml
```

### Containers não iniciam
```bash
# Ver logs
docker-compose logs

# Reiniciar
docker-compose down
docker-compose up -d
```

### WhatsApp não conecta
- Verifique se o QR Code foi escaneado
- Confirme se o número está no formato correto (com código do país)
- Aguarde alguns segundos após escanear o QR Code

---

**⏱️ Tempo estimado de configuração**: 5-10 minutos
