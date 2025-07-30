# Site Omega - E-commerce de Produtos da Engenharia

## Visão Geral

O site Omega é uma plataforma de e-commerce desenvolvida especificamente para a venda de produtos da engenharia IFSULDEMINAS - Poços de Caldas. O site oferece uma experiência completa de compra online com carrinho de compras, personalização de produtos e integração com o Mercado Pago.

## Características Principais

### ✅ Funcionalidades Implementadas

- **Design Responsivo**: Compatível com desktop e mobile
- **Identidade Visual**: Cores #F1404C (vermelho) e branco com detalhes pretos
- **Catálogo de Produtos**: Camisetas, combos e acessórios
- **Personalização**: Camisetas podem ser personalizadas com nomes
- **Tabela de Tamanhos**: P, M, G, GG para produtos aplicáveis
- **Carrinho de Compras**: Adicionar, remover e alterar quantidades
- **Sistema de Desconto**: 5% de desconto para pagamento via PIX
- **Combos**: Produtos com desconto já aplicado
- **Formas de Pagamento**:
  - PIX (5% desconto)
  - Cartão de Débito (valor total)
  - Cartão de Crédito (até 3x sem juros)
- **Formulário de Cliente**: Nome completo, email e telefone
- **Integração Mercado Pago**: Preparado para pagamentos online

### 🎨 Design e Interface

- Banner principal com mascote da Omega
- Layout inspirado em grandes e-commerces
- Navegação intuitiva e responsiva
- Cards de produtos com informações claras
- Modal de detalhes do produto
- Carrinho lateral deslizante
- Footer informativo

## Estrutura do Projeto

```
omega_ecommerce/
├── frontend/
│   └── omega-store/          # Aplicação React
│       ├── src/
│       │   ├── components/   # Componentes React
│       │   ├── assets/       # Imagens e recursos
│       │   └── config.js     # Configurações da API
├── backend/
│   └── omega-api/            # API Flask
│       ├── src/
│       │   ├── models/       # Modelos de dados
│       │   ├── routes/       # Rotas da API
│       │   └── main.py       # Arquivo principal
└── assets/                   # Recursos do projeto
```

## Tecnologias Utilizadas

### Frontend
- **React 18**: Framework JavaScript
- **Vite**: Build tool e servidor de desenvolvimento
- **Tailwind CSS**: Framework CSS para estilização
- **Lucide React**: Ícones
- **shadcn/ui**: Componentes de interface

### Backend
- **Flask**: Framework Python para API
- **SQLAlchemy**: ORM para banco de dados
- **Flask-CORS**: Suporte a CORS
- **SQLite**: Banco de dados

### Integração
- **Mercado Pago API**: Sistema de pagamentos
- **Requests**: Cliente HTTP para Python

## Como Executar o Projeto

### Pré-requisitos
- Node.js 20+
- Python 3.11+
- npm ou yarn

### Backend (API Flask)

1. Navegue até a pasta do backend:
```bash
cd omega_ecommerce/backend/omega-api
```

2. Ative o ambiente virtual:
```bash
source venv/bin/activate
```

3. Instale as dependências (se necessário):
```bash
pip install flask flask-cors requests
```

4. Execute o servidor:
```bash
python src/main.py
```

O backend estará disponível em: `http://localhost:5000`

### Frontend (React)

1. Navegue até a pasta do frontend:
```bash
cd omega_ecommerce/frontend/omega-store
```

2. Instale as dependências:
```bash
npm install
```

3. Execute o servidor de desenvolvimento:
```bash
npm run dev -- --host
```

O frontend estará disponível em: `http://localhost:5173`

## Configuração do Mercado Pago

Para configurar o Mercado Pago em produção:

1. Obtenha suas credenciais no [Mercado Pago Developers](https://www.mercadopago.com.br/developers)
2. Configure as variáveis de ambiente:
```bash
export MERCADOPAGO_ACCESS_TOKEN="seu_access_token"
export MERCADOPAGO_PUBLIC_KEY="sua_public_key"
```

## Produtos Disponíveis

### Camisetas
- **Camiseta Omega Preta**: R$ 45,00 (Personalizável)
- **Camiseta Omega Vermelha**: R$ 45,00 (Personalizável)
- Tamanhos: P, M, G, GG

### Combos
- **Combo Omega - 3 Camisetas**: R$ 120,00 (De R$ 135,00)
- Tamanhos: P, M, G, GG

### Acessórios
- **Caneca Omega**: R$ 25,00

## Formas de Pagamento

| Método | Desconto | Parcelas |
|--------|----------|----------|
| PIX | 5% | À vista |
| Débito | - | À vista |
| Crédito | - | Até 3x sem juros |

## Funcionalidades Futuras

- [ ] Sistema de estoque em tempo real
- [ ] Histórico de pedidos
- [ ] Sistema de avaliações
- [ ] Cupons de desconto
- [ ] Programa de fidelidade
- [ ] Chat de atendimento
- [ ] Rastreamento de pedidos

## Suporte e Manutenção

Para suporte técnico ou dúvidas sobre o sistema:
- Documentação da API: Disponível em `/api/docs` (quando implementada)
- Logs do sistema: Verificar console do navegador e logs do Flask

## Licença

Este projeto foi desenvolvido exclusivamente para a engenharia IFSULDEMINAS - Poços de Caldas.

---

**Desenvolvido com ❤️ para a Omega Engineering**

