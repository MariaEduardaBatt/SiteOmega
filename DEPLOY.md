# Guia de Deploy - Site Omega

## Deploy em Produção

### Opção 1: Deploy Automático (Recomendado)

O projeto está preparado para deploy automático usando as ferramentas do sandbox:

#### Frontend (React)
```bash
cd omega_ecommerce/frontend/omega-store
npm run build
# Use a ferramenta de deploy do frontend
```

#### Backend (Flask)
```bash
cd omega_ecommerce/backend/omega-api
# Use a ferramenta de deploy do backend
```

### Opção 2: Deploy Manual

#### Preparação do Frontend
1. Build da aplicação React:
```bash
cd omega_ecommerce/frontend/omega-store
npm run build
```

2. Os arquivos estarão na pasta `dist/`

#### Preparação do Backend
1. Configure as variáveis de ambiente:
```bash
export MERCADOPAGO_ACCESS_TOKEN="seu_token_producao"
export MERCADOPAGO_PUBLIC_KEY="sua_chave_publica"
export FLASK_ENV="production"
```

2. Para deploy em serviços como Heroku, Railway, ou DigitalOcean:
```bash
# Instale gunicorn para produção
pip install gunicorn

# Execute com gunicorn
gunicorn -w 4 -b 0.0.0.0:5000 src.main:app
```

## Configurações Importantes

### Mercado Pago
- Substitua as credenciais de teste pelas de produção
- Configure os webhooks para receber notificações de pagamento
- Teste todos os fluxos de pagamento antes do lançamento

### Banco de Dados
- Em produção, considere usar PostgreSQL ou MySQL
- Configure backups automáticos
- Implemente migrações de banco de dados

### Segurança
- Use HTTPS em produção
- Configure CORS adequadamente
- Implemente rate limiting
- Use variáveis de ambiente para credenciais

### Monitoramento
- Configure logs de aplicação
- Implemente monitoramento de uptime
- Configure alertas para erros

## Checklist de Deploy

- [ ] Credenciais do Mercado Pago configuradas
- [ ] Build do frontend gerado
- [ ] Variáveis de ambiente configuradas
- [ ] HTTPS configurado
- [ ] Domínio configurado
- [ ] Testes de pagamento realizados
- [ ] Backup do banco de dados configurado
- [ ] Monitoramento ativo

## URLs de Produção

Após o deploy, o site estará disponível em:
- Frontend: `https://seu-dominio.com`
- API: `https://api.seu-dominio.com`

## Manutenção

### Atualizações
1. Faça backup do banco de dados
2. Teste as alterações em ambiente de desenvolvimento
3. Deploy das alterações
4. Verifique se tudo está funcionando

### Backup
- Configure backup automático diário do banco de dados
- Mantenha backups dos arquivos de configuração
- Teste a restauração periodicamente

## Suporte Pós-Deploy

Para questões técnicas após o deploy:
1. Verifique os logs da aplicação
2. Teste as funcionalidades principais
3. Monitore as métricas de performance
4. Mantenha as dependências atualizadas

