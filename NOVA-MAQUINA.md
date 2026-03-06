# 🚀 GUIA DE MIGRAÇÃO — NOVA MÁQUINA
### Recuperar JARVIS + MEGA BRAIN do zero

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                                                                              ║
║   ██╗ █████╗ ██████╗ ██╗   ██╗██╗███████╗                                   ║
║   ██║██╔══██╗██╔══██╗██║   ██║██║██╔════╝                                   ║
║   ██║███████║██████╔╝██║   ██║██║███████╗                                   ║
║   ██║██╔══██║██╔══██╗╚██╗ ██╔╝██║╚════██║                                   ║
║   ██║██║  ██║██║  ██║ ╚████╔╝ ██║███████║                                   ║
║   ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝  ╚═══╝  ╚═╝╚══════╝                                   ║
║                                                                              ║
║              NOVA MÁQUINA → SISTEMA COMPLETO EM 20 MINUTOS                  ║
║                                                                              ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

---

## 📦 O QUE VOCÊ PRECISA TER NO PENDRIVE

Antes de começar, confirme que tem esses 2 itens:

```
pendrive/
├── 📁 MEGABRAIN/          ← pasta completa do projeto
└── 📄 .gdrive-credentials.json   ← credenciais Google Drive
```

> ⚠️ Se não tiver o `.gdrive-credentials.json`, não se preocupe — você vai reautenticar no passo 6.

---

## 🛠️ FASE 1 — INSTALAR DEPENDÊNCIAS

### 1.1 Git
```
https://git-scm.com/download/win
```
- Baixar → instalar com opções padrão
- Testar: abrir terminal e digitar `git --version`

### 1.2 Node.js (versão LTS)
```
https://nodejs.org
```
- Baixar a versão **LTS** → instalar
- Testar: `node --version` e `npm --version`

### 1.3 Python 3
```
https://www.python.org/downloads/
```
- Baixar → instalar marcando ✅ **"Add Python to PATH"**
- Testar: `python --version`

---

## 📂 FASE 2 — RESTAURAR O PROJETO

### 2.1 Copiar a pasta MEGABRAIN

Cole a pasta do pendrive em:
```
C:\Users\{seu_usuario}\OneDrive\Documentos\MEGABRAIN
```

### 2.2 Instalar dependências do projeto

Abrir terminal na pasta MEGABRAIN e rodar:
```bash
npm install
```

### 2.3 Instalar dependências Python
```bash
pip install -r requirements.txt
```

---

## 🤖 FASE 3 — INSTALAR CLAUDE CODE

```bash
npm install -g @anthropic-ai/claude-code
```

Testar:
```bash
claude --version
```

---

## 🔑 FASE 4 — RESTAURAR CREDENCIAIS

### 4.1 Arquivo `.gdrive-credentials.json`

**Se você trouxe no pendrive:**
- Cole o arquivo em:
```
C:\Users\{seu_usuario}\.gdrive-credentials.json
```

**Se não trouxe (reautenticação):**
- Abrir terminal na pasta MEGABRAIN e rodar:
```bash
python auth_gdrive.py
```
- Vai abrir o navegador → fazer login com sua conta Google → autorizar
- O arquivo será criado automaticamente

### 4.2 Atualizar path no `.mcp.json`

Se o nome do usuário na nova máquina for diferente de `naiar`:

Abrir `.mcp.json` na raiz do MEGABRAIN e atualizar:
```json
"GDRIVE_CREDENTIALS_PATH": "C:\\Users\\{NOVO_USUARIO}\\.gdrive-credentials.json",
"GDRIVE_OAUTH_PATH": "C:\\Users\\{NOVO_USUARIO}\\OneDrive\\Documentos\\MEGABRAIN\\gcp-oauth.keys.json"
```

---

## ✅ FASE 5 — TESTAR TUDO

Abrir terminal na pasta MEGABRAIN:
```bash
claude
```

Quando o Claude Code abrir, **copie e cole exatamente essa mensagem:**

---

## 💬 O QUE FALAR PARA O JARVIS NA NOVA MÁQUINA

```
Olá JARVIS. Nova máquina configurada.

Por favor:
1. Leia o arquivo .claude/sessions/LATEST-SESSION.md
2. Me dê um briefing completo do que estava sendo trabalhado
3. Confirme que o sistema está funcionando corretamente
4. Liste qualquer pendência ou próximo passo registrado

Estamos prontos para continuar.
```

---

## 🗺️ ESTRUTURA DO SISTEMA (para referência)

```
MEGABRAIN/
│
├── 🧠 .claude/
│   ├── sessions/          ← histórico de todas as sessões
│   ├── skills/            ← habilidades do JARVIS
│   ├── hooks/             ← automações
│   └── rules/             ← regras do sistema
│
├── 🤖 agents/             ← agentes de IA (Cargo + Persons)
├── 📚 knowledge/          ← base de conhecimento extraída
├── 📥 inbox/              ← materiais para processar
├── 📊 artifacts/          ← outputs do pipeline
│
├── 🔐 .env                ← suas API keys (nunca commitar)
├── 🔐 .mcp.json           ← configuração MCP (Google Drive, etc.)
└── 🌐 index.html          ← dashboard público (GitHub Pages)
```

---

## 🔗 LINKS IMPORTANTES

| Item | Link |
|------|------|
| **Repositório** | https://github.com/piterclark/JARVIS |
| **Dashboard público** | https://piterclark.github.io/JARVIS |
| **Claude Code docs** | https://docs.anthropic.com/claude-code |

---

## ❓ PROBLEMAS COMUNS

| Problema | Solução |
|----------|---------|
| `claude: command not found` | Rodar `npm install -g @anthropic-ai/claude-code` |
| MCP Google Drive não conecta | Verificar path do `.gdrive-credentials.json` no `.mcp.json` |
| Python não encontrado | Reinstalar marcando "Add to PATH" |
| MEGABRAIN não aparece | Aguardar OneDrive sincronizar (5-10 minutos) |
| JARVIS não lembra nada | Ler `.claude/sessions/LATEST-SESSION.md` manualmente |

---

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                                                                              ║
║   Sistema restaurado com sucesso?  →  Diga "JARVIS online" e continue.      ║
║                                                                              ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

---
*Gerado em: 2026-03-06 | Sistema: MEGA BRAIN + JARVIS | Repositório: piterclark/JARVIS*
