# App nativo (Capacitor) — Android e iOS

Empacota o sistema como app nativo de verdade: instala por arquivo, tem ícone próprio
e **funciona por http, direto no IP da fábrica** — sem precisar de https nem de túnel.

## Configurar
Troque o endereço do servidor em `capacitor.config.json`:

    "url": "http://192.168.0.101:8503"

Fixe esse IP no roteador, senão o app para de achar o servidor quando ele mudar.

## Gerar o APK sem instalar nada
1. Suba a pasta `nativo` (com o `.github`) para um repositório no GitHub.
2. Actions > "Build APK (Capacitor)" > Run workflow.
3. Baixe o `.apk` em Artifacts e mande por WhatsApp.

## Gerar no seu computador
Precisa de Node.js e Android Studio:

    cd nativo
    npm run preparar
    npm run abrir        # Build > Build APK(s)

## iPhone
    npx cap add ios
Precisa de um Mac com Xcode. Publicar exige conta Apple Developer (US$ 99/ano).
Sem Mac, o caminho do iPhone continua sendo o PWA pelo Safari.

## Notificações dentro do app nativo
O app usa notificações locais: enquanto ele está aberto ou em segundo plano recente,
os chamados novos avisam com som e vibração. Aviso com o app fechado por horas
exige Firebase (Android) e APNs (iPhone) — aí entra internet e conta de desenvolvedor.
