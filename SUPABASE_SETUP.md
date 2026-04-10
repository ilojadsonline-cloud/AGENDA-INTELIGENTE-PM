# Setup do Supabase

## Quando usar cada SQL

- Use `supabase/schema.sql` se o projeto Supabase estiver novo ou se voce ainda nao executou o schema antigo.
- Use `supabase/migration-from-profile-id.sql` se voce ja executou a versao anterior baseada em `profile_id`.

## Variaveis de ambiente

Crie um arquivo `.env.local` na raiz:

```env
VITE_SUPABASE_URL=sua_url_do_projeto
VITE_SUPABASE_PUBLISHABLE_KEY=sua_chave_publishable
```

## Passos no painel do Supabase

1. Abra `Auth > Providers` e confirme que `Email` esta habilitado.
2. Em `Auth > URL Configuration`, defina a `Site URL`.
3. Para desenvolvimento local, use `http://localhost:5173` como `Site URL` ou adicione nas redirect URLs.
4. Rode o SQL adequado no `SQL Editor`.

## Fluxos prontos no app

- Login com e-mail e senha
- Cadastro de nova conta
- Recuperacao de senha por e-mail
- Logout
- Persistencia de dados por usuario autenticado

## Executar localmente

```bash
npm run dev
```

## Observacao importante

Se a confirmacao de e-mail estiver habilitada no projeto Supabase, usuarios novos podem precisar confirmar o e-mail antes do primeiro login completo.
