# APK do Operação Vectra

## 1. Ajustar o endereço do servidor
Abra `capacitor.config.json` e troque o IP pelo do seu servidor:

    "url": "http://192.168.0.101:8503"

## 2. Subir para o GitHub
Crie um repositório e envie TODOS os arquivos desta pasta, mantendo a estrutura:

    .github/workflows/apk.yml     <- é este arquivo que cria o botão Build APK
    capacitor.config.json
    package.json
    www/index.html

Se o GitHub não aceitar a pasta .github ao arrastar, use
"Add file > Create new file", digite  .github/workflows/apk.yml  no nome
e cole o conteúdo do arquivo.

## 3. Gerar
Aba Actions > Build APK > Run workflow. Em uns 5 minutos, baixe o Artifact.

## 4. Instalar
Mande o .apk por WhatsApp. No celular, toque no arquivo e autorize
"instalar apps desconhecidos" para o app de onde veio.
O celular precisa estar no mesmo Wi-Fi do servidor.
