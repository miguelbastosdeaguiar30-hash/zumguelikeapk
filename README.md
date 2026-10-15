# Zumguelike para Android (Capacitor)

Este projeto envolve o HTML original do jogo em um aplicativo Android usando Capacitor. O jogo original está em `www/index.html`.

## Compilar APK grátis pelo GitHub Actions

1. Crie um repositório GitHub e envie **todos os arquivos desta pasta** para a branch `main` (não envie só o HTML).
2. Abra a aba **Actions** do repositório.
3. Se o GitHub pedir, habilite workflows.
4. Selecione **Build Zumguelike APK** e toque em **Run workflow**. Um push na `main` também inicia a compilação.
5. Quando o processo ficar verde como **Success**, abra a execução e procure **Artifacts**.
6. Baixe `Zumguelike-debug-apk.zip`, extraia o ZIP e encontre `app-debug.apk`.
7. Transfira o APK ao Android e instale. O Android pode pedir autorização para instalar apps dessa fonte.

## Observações importantes

- Este é um **APK debug para testes**, não uma versão assinada para publicação na Play Store.
- O HTML original usa Firebase Authentication e Firestore do projeto `zumguelike`. A configuração existente foi mantida.
- Login por e-mail/senha deve ser testado no APK. O login Google usa `signInWithPopup`, que pode não funcionar dentro de um WebView/Capacitor; pode precisar de integração nativa se quiser usar Google login no app.
- Confirme no Firebase Console que `localhost`/domínios aplicáveis e os provedores de login estão configurados. O domínio autorizado não é uma solução universal para o login Google dentro do APK.
- Não alterei a lógica do jogo nem suas regras do Firebase; este pacote é apenas a estrutura de compilação Android.
