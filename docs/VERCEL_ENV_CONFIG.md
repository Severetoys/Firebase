# Configuração de Variáveis de Ambiente no Vercel

## ⚠️ SECURITY UPDATE
**IMPORTANT:** All Firebase configuration values are now environment variables for security. Never commit real API keys to your repository. Use the values from your local `.env.local` file when configuring deployment environments.

## ⚠️ PROBLEMA RESOLVIDO
O erro "Environment Variable references Secret which does not exist" foi causado pelo arquivo `vercel.json` que referenciava secrets não existentes.

## ✅ SOLUÇÃO APLICADA
1. **Removido referências de secrets** do `vercel.json`
2. **Criado `.env.production`** com todas as variáveis
3. **Configuração manual necessária** no painel do Vercel

## 🔧 COMO CONFIGURAR NO VERCEL

### 1. Acesse o Painel do Vercel
- Vá para: https://vercel.com/dashboard
- Selecione seu projeto: `studio`

### 2. Configure as Variáveis de Ambiente
- Clique em **Settings** > **Environment Variables**
- Adicione TODAS as variáveis abaixo:

### 🔥 Firebase Configuration (Use your actual values from .env.local)
```
NEXT_PUBLIC_FIREBASE_API_KEY = your_api_key_here
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN = your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID = your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET = your_project.firebasestorage.app
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID = your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID = your_app_id
NEXT_PUBLIC_FIREBASE_DATABASE_URL = https://your_project-default-rtdb.firebaseio.com
NEXT_PUBLIC_FIREBASE_MEASUREMENT_ID = your_measurement_id
```

### 💰 Payment Systems
```
MERCADOPAGO_PUBLIC_KEY = APP_USR-e9289eca-b8bd-4677-9481-bc9f6388eb67
MERCADOPAGO_ACCESS_TOKEN = APP_USR-1595377099020994-122510-cd38e362938f5ca604774d3efa719cbe-696581588
NEXT_PUBLIC_PAYPAL_CLIENT_ID = AXykIWKfbbsR_Qe4eLrDgxudUWcoFn-cihQdgWJTqEOVQiP5fxXln-C5fr1QABQ4jowP7Oz2nkNtPFie
PAYPAL_CLIENT_SECRET = EGcfrzzmrL_jpRt-9kp2GaaF3f7jVNvOg4EHVwsnMl4V28_0iyN0UXu5OGvAT1c9e_OeikFuWe8QqSlX
NEXT_PUBLIC_PAYPAL_BUSINESS_EMAIL = pix@italosantos.com
```

### 🌍 Environment
```
NEXT_PUBLIC_ENVIRONMENT = production
```

### 🔑 API Keys
```
TWITTER_BEARER_TOKEN = AAAAAAAAAAAAAAAAAAAAAEebugEAAAAA54Zk%2BYxiPsyxHQdrsWm5enS8C9M%3DkOVn6m1pvz8wb1jqM9QQTLpeFs7QyZvOeJycHfjXdrDw7M378z
INSTAGRAM_FEED_ACCESS_TOKEN = IGAAKe7p2HuutBZAFBpWHNBcWFmOXlOWVFiMS1yODN6elprU1oxRlZAtb0UxMnRZATFdSN0JLbUZASMXJpMElmLXhZARVRuWHNJYTNRcGt5blNWYlczb3FWYzcxemQ3Y2pkaHg1NkVSMzBDc21JRENpMTl2dGxNMzFPZATBWdHBCUW1TZAwZDZD
INSTAGRAM_SHOP_ACCESS_TOKEN = IGAAKe7p2HuutBZAE14YkM0TVZACbldrWW4zZAktYclFPb1c3ZADQ5emFhNjFJOEI2MFlHMGxlWXRxR2ExSmpSZADg4MTBNcVMtTkxoNzhMODFaMnpnMnZAnNG1RUGNXcHpQTGVoaF9uNTBsbENFaGV0Mm84bkpGTWJFR1FFMnhOSm5VOAZDZD
FACEBOOK_PAGE_ACCESS_TOKEN = YOUR_FACEBOOK_PAGE_ACCESS_TOKEN
GEMINI_API_KEY = AIzaSyDsUxT8enFtbfWFQKUCkvL6dj9W0e7KXoA
```

### 3. Ambiente de Deploy
Para cada variável, selecione:
- ✅ **Production**
- ✅ **Preview**
- ✅ **Development**

### 4. Redeploy
Após configurar, faça:
- Push para branch `dev6`
- Ou clique em **Redeploy** no painel

## 🚀 RESULTADO
- ✅ Erro de secrets resolvido
- ✅ Variáveis de ambiente configuradas
- ✅ Deploy funcionará corretamente
- ✅ PayPal, MercadoPago e Firebase funcionando

## 📝 NOTAS
- Todas as credenciais são de **PRODUÇÃO**
- Firebase configurado para o projeto `authkit-y9vjx`
- PayPal usando credenciais live
- MercadoPago usando credenciais de produção
