# Aula MCP

Servidor MCP em Python para consultar documentos armazenados no Supabase.

## Visão geral

Este projeto expõe ferramentas, resources e prompts para consultar a tabela `public.documentos` usando o protocolo MCP. Ele lê configurações do arquivo `.env` e faz requisições HTTP para a API do Supabase.

## Requisitos

- Python 3.11+
- pip ou uv
- Conta e projeto Supabase configurados

## Configuração inicial

1. Clone o repositório:

```bash
git clone https://github.com/heltonrolim/aula-mcp.git
cd aula-mcp
```

2. Crie e ative um ambiente virtual:

### Windows (PowerShell)

```powershell
py -3.13 -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### macOS/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. Instale as dependências:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Ou com uv:

```bash
uv sync
```

## Variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto com base no exemplo:

```env
SUPABASE_URL=https://SEU_PROJETO.supabase.co
SUPABASE_API_TOKEN=SEU_TOKEN
SUPABASE_REF_PROJECT=SEU_REF_DO_PROJETO
```

Você pode usar o arquivo [.env.example](.env.example) como modelo.

## Executando o servidor

```bash
python server.py
```

Ou usando uv:

```bash
uv run mcp dev server.py
```

## Estrutura do projeto

```text
.
├── .env.example
├── .gitignore
├── README.md
├── requirements.txt
├── server.py
└── package.json
```

## Observações

- O arquivo `.env` nunca deve ser enviado para o GitHub.
- O projeto já possui `.gitignore` configurado para ignorar `.env`, `.venv`, `__pycache__`, entre outros.
- Ajuste os valores das variáveis de ambiente antes de iniciar o servidor.

## Licença

Este projeto é para uso educacional e pessoal.
