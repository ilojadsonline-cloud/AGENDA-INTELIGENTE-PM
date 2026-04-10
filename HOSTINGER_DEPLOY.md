# Deploy na Hostinger

## O que este projeto usa

- Build: `npm run build`
- Start: `npm start`
- Porta: definida pela variavel `PORT` da Hostinger

## Configuracao recomendada na Hostinger

Se estiver usando a implantacao Node.js via GitHub:

- Node.js version: `20`, `22` ou `24`
- Build command: `npm install && npm run build`
- Start command: `npm start`

## Variaveis de ambiente obrigatorias

Adicione no painel da Hostinger:

- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_PUBLISHABLE_KEY`

Valores:

- `VITE_SUPABASE_URL=https://zaegwfzrmwhxizthrxyv.supabase.co`
- `VITE_SUPABASE_PUBLISHABLE_KEY=...`

## Muito importante

O arquivo `.env.local` fica no seu computador e normalmente nao vai para o GitHub.
Por isso, mesmo que funcione localmente, a Hostinger precisa dessas variaveis
configuradas no painel para conseguir gerar o build correto.

## Se der erro no deploy

Confira estes pontos:

1. O repositório contem `package.json` na raiz
2. A versao do Node selecionada e compativel
3. As variaveis do Supabase foram configuradas no painel
4. O projeto esta sendo tratado como Node.js app, nao como upload manual de arquivos crus
5. O log do build mostra se a falha ocorreu em `npm install`, `npm run build` ou `npm start`
