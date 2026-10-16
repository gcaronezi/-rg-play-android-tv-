# Gerar o APK usando apenas o celular

Este projeto ainda não contém um APK compilado. O workflow `.github/workflows/build-apk.yml` permite compilar o projeto em um serviço de build online, sem instalar Android Studio no celular.

## Passos
1. No navegador do celular, entre em https://github.com e crie uma conta ou entre na sua.
2. Crie um repositório novo (por exemplo, `rg-play-android-tv`).
3. Extraia o ZIP do projeto e envie os arquivos e pastas para o repositório. Inclua a pasta oculta `.github/workflows`.
4. Abra a aba **Actions**, selecione **Build R&G Play APK** e toque em **Run workflow**.
5. Quando terminar com sucesso, abra a execução e baixe o artefato **RG-Play-AndroidTV-debug-apk**. Ele contém `app-debug.apk`.

Observações:
- O build online precisa terminar com sucesso; este arquivo não é garantia de que o aplicativo esteja livre de erros.
- O APK de depuração não é publicado na Play Store e não está assinado para distribuição comercial.
- A conectividade com servidores e a reprodução de vídeo ainda precisam ser testadas em uma TV Box real.
- Use apenas serviços e listas para os quais você tem autorização de acesso.
