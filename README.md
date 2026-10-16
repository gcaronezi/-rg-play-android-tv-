# R&G Play — Android TV project (v0.3.0)

Este é o projeto-fonte Android Studio que empacota o protótipo Xtream existente numa Activity de tela cheia, com suporte a Android TV/TV Box e navegação por controle remoto via WebView.

## O que está incluído
- App Android com categorias de launcher normal e Android TV (Leanback).
- Tela horizontal, modo imersivo e WebView com JavaScript/DOM storage habilitados.
- Protótipo Xtream original em `app/src/main/assets/index.html`.
- Tela de login, catálogo quando a API é compatível, busca, categorias e migração manual de servidores.

## Como gerar o APK
1. Abra a pasta `RG_Play_AndroidTV_Project` no Android Studio (versão recente).
2. Aguarde a sincronização do Gradle e instale o Android SDK Platform 35 se solicitado.
3. Use **Build > Build APK(s)**.
4. O APK de depuração normalmente será criado em `app/build/outputs/apk/debug/app-debug.apk`.

## Limitações e segurança
- Este ambiente não tem Android SDK/Gradle configurado para compilar e testar um APK aqui; por isso esta entrega é o projeto-fonte, não um APK compilado.
- A interface usa WebView; reprodução de streams pode variar conforme formato, codecs, DRM e restrições do provedor. Alguns serviços bloqueiam requisições feitas pelo navegador por CORS. Para compatibilidade mais robusta, a próxima etapa é substituir o player HTML por AndroidX Media3/ExoPlayer e implementar as chamadas de API nativamente.
- A migração incluída é manual: você precisa ter autorização e dados de acesso para cada servidor. O app não descobre automaticamente servidores ativos.
- Use apenas serviços e conteúdos que você esteja autorizado a acessar. Não compartilhe credenciais com terceiros.
- `usesCleartextTraffic=true` foi habilitado para compatibilidade com servidores legados HTTP. Para uma versão de produção, prefira HTTPS e restrinja tráfego inseguro quando possível.
