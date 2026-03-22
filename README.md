# Planly — Deploy no Vercel

## Estrutura do projeto
```
planly/
├── index.html       ← app principal
├── api/
│   └── chat.js      ← proxy que esconde sua API key
└── vercel.json      ← config do Vercel
```

## Passo a passo (10 minutos)

### 1. Crie uma conta no Vercel
Acesse https://vercel.com e crie conta com seu GitHub ou Google.

### 2. Instale o Vercel CLI (opcional, mais fácil via GitHub)
Ou use o método direto abaixo.

### 3. Suba o projeto via GitHub
1. Crie um repositório no GitHub (pode ser privado)
2. Suba os 3 arquivos: `index.html`, `api/chat.js`, `vercel.json`
3. No Vercel, clique em "Add New Project"
4. Conecte seu GitHub e selecione o repositório

### 4. Configure a variável de ambiente (SUA API KEY)
No painel do Vercel, antes de fazer deploy:
- Vá em **Settings → Environment Variables**
- Adicione:
  - **Name:** `ANTHROPIC_API_KEY`
  - **Value:** `sk-ant-sua-chave-aqui`
- Clique em Save

### 5. Deploy
Clique em **Deploy**. Em 2 minutos seu link estará no ar.
Ex: `https://planly.vercel.app`

## Trial de 30 dias
O trial é controlado pelo navegador do usuário (localStorage).
Após 30 dias, ele vê a tela de upgrade e é redirecionado para planly.com.br.

## Custos estimados
- Vercel: **gratuito** (plano hobby)
- Anthropic API: ~R$ 0,02 por dashboard gerado
- 100 usuários × 10 dashboards/mês = ~R$ 20/mês de custo de API

## Próximo passo (produto completo)
- Login com Supabase
- Cobrança com Kiwify ou Stripe
- Email automático com OAuth Google
- Histórico de dashboards
