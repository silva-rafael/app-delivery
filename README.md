# 🍔 Lanchonete Delivery System

[![Python Version](https://img.shields.io/badge/python-3.10+-blue.svg)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-green.svg)](https://fastapi.tiangolo.com)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)](https://streamlit.io)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL-3ECF8E.svg)](https://supabase.com)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Um sistema completo para gerenciamento de pedidos e entregas em lanchonetes, com interface para clientes, dashboard administrativo e app para entregadores.

## ✨ Demonstração

<div align="center">
  <img src="docs/images/dashboard-preview.png" alt="Dashboard Preview" width="800">
  <br>
  <em>Dashboard Administrativo</em>
</div>

## 🚀 Funcionalidades

### 👤 Para Clientes
- ✅ Catálogo de produtos com categorias
- ✅ Carrinho de compras intuitivo
- ✅ Finalização de pedido com endereço
- ✅ Acompanhamento em tempo real
- ✅ Histórico de pedidos
- ✅ QR Code para rastreamento rápido

### 👨‍💼 Para Administradores
- 📊 Dashboard com métricas em tempo real
- 🍔 CRUD completo de produtos
- 📦 Gerenciamento de pedidos
- 🛵 Atribuição de entregadores
- 📈 Relatórios de vendas (PDF/Excel)
- 💰 Controle de faturamento

### 🛵 Para Entregadores
- 📱 Interface mobile-first
- 🗺️ Visualização de pedidos atribuídos
- ✅ Atualização de status de entrega
- 💵 Histórico de ganhos
- 📍 Rastreamento de localização (em breve)

## 🎯 Tecnologias Utilizadas

### Backend
- **FastAPI** - Framework web assíncrono
- **Supabase** - Banco de dados PostgreSQL + Realtime
- **Python 3.10+** - Linguagem principal
- **Pydantic** - Validação de dados

### Frontend
- **Streamlit** - Dashboard administrativo
- **HTML5/CSS3** - Interface do cliente
- **JavaScript Puro** - Interatividade
- **Responsive Design** - Mobile-first

### Ferramentas
- **Docker** - Containerização
- **GitHub Actions** - CI/CD
- **Pytest** - Testes automatizados

## 📦 Instalação Rápida

### Pré-requisitos

- Python 3.10 ou superior
- Conta no [Supabase](https://supabase.com) (gratuita)
- Git

### Passo a Passo

```bash
# 1. Clone o repositório
git clone https://github.com/seu-usuario/lanchonete-delivery.git
cd lanchonete-delivery

# 2. Configure o ambiente virtual
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate  # Windows

# 3. Instale as dependências
cd backend
pip install -r requirements.txt

# 4. Configure as variáveis de ambiente
cp .env.example .env
# Edite o .env com suas credenciais do Supabase

# 5. Execute as migrações do banco
python -c "from database.schema import init_db; init_db()"

# 6. Inicie a aplicação
uvicorn main:app --reload --port 8000 &  # Backend
streamlit run frontend/admin/dashboard.py  # Admin
# Abra o frontend/cliente/index.html no navegador
