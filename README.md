# VaultFile

Gerenciador de arquivos para Android desenvolvido com Flutter, com navegação local, edição de texto e código, visualização de mídia, compactação, criptografia e conexões FTP/FTPS.

## Visão geral

O VaultFile centraliza tarefas comuns de gerenciamento de arquivos em uma interface limpa e organizada. O aplicativo trabalha com o armazenamento local do dispositivo e oferece ferramentas para editar, organizar, proteger e compartilhar arquivos.

## Recursos

### Gerenciamento local

- Navegação por pastas, subpastas e armazenamento interno
- Acesso rápido a Downloads, Imagens e Vídeos
- Visualização em lista, quadrados ou lista detalhada
- Pesquisa por nome
- Exibição opcional de arquivos ocultos
- Seleção individual ou múltipla
- Criar pastas
- Renomear arquivos e pastas
- Mover itens para outra pasta
- Apagar um ou vários itens
- Compartilhar usando o menu nativo do Android
- Abrir arquivos com outros aplicativos
- Visualização de extensão, tipo, tamanho, caminho, data e permissões

### Edição de arquivos

O editor interno suporta arquivos de texto, configuração, código e dados, incluindo:

`.txt`, `.md`, `.log`, `.ini`, `.cfg`, `.conf`, `.config`, `.env`, `.properties`, `.toml`, `.yaml`, `.yml`, `.xml`, `.json`, `.csv`, `.tsv`, `.db`, `.html`, `.htm`, `.css`, `.scss`, `.sass`, `.js`, `.mjs`, `.cjs`, `.jsx`, `.ts`, `.tsx`, `.php`, `.py`, `.java`, `.c`, `.h`, `.cpp`, `.hpp`, `.cs`, `.go`, `.rs`, `.rb`, `.swift`, `.kt`, `.dart`, `.sql`, `.sh`, `.bash`, `.ps1`, `.bat`, `.cmd`, `.lua`, `.pl`, `.r`, `.ex`, `.exs`, `.vue`, `.svelte`, `.diff`, `.patch`, `.tex`, `.rtf`, `.svg`, `.graphql`, `.gql`, `.proto`, `.ipynb`, `.lock`, `.gitignore`, `.gitattributes`, `.editorconfig`, `.dockerignore`, `Makefile` e `Dockerfile`.

Arquivos HTML podem ser visualizados em uma prévia renderizada dentro do aplicativo.

### Imagens

- Visualização com zoom
- Editor interno com caneta
- Cores de desenho
- Controle de espessura
- Desfazer traços
- Salvamento como nova cópia editada
- Suporte a JPG, JPEG, PNG, GIF, WEBP, BMP, TIFF, HEIC, HEIF, AVIF e ICO

### Áudio e vídeo

- Player interno para MP3, WAV, M4A, AAC, OGG e FLAC
- Interface de áudio com capa visual, progresso, duração e controles
- Player de vídeo para MP4, MOV, MKV e AVI
- Pausar e continuar reprodução
- Abertura com outro aplicativo para edição avançada

### Compactação

- Criar arquivos ZIP
- Compactar um ou vários itens
- Extrair ZIP dentro do VaultFile
- Abrir ZIP com outro aplicativo
- Ações contextuais para UnRAR e extração de 7Z usando um compactador instalado no Android

A biblioteca interna oferece criação e extração de ZIP. RAR e 7Z são encaminhados ao aplicativo compatível escolhido pelo sistema, pois esses formatos dependem de bibliotecas nativas específicas.

### Criptografia

- Criptografar qualquer arquivo com senha
- Formato protegido com extensão `.vault`
- Descriptografar mediante senha
- Senha não é armazenada pelo aplicativo
- Arquivo original preservado durante a criptografia
- Criptografia AES com chave derivada por SHA-256

### FTP e FTPS

- Cadastro de até 10 contas
- Nome personalizado
- Host por IP ou domínio
- Porta configurável
- Usuário e senha
- Alternância entre FTP e FTPS
- Teste de conexão
- Persistência local das contas

## Aparência

O aplicativo oferece quatro temas:

- Claro
- Cinza
- Escuro
- Glassmorphism, com transparência, gradientes e desfoque inspirados em interfaces móveis modernas

A preferência fica salva localmente.

## Permissões Android

O aplicativo pode solicitar permissões relacionadas a armazenamento, gerenciamento amplo de arquivos, câmera, localização, fotos, vídeos, áudio, notificações e conexões de rede. A disponibilidade de algumas permissões depende da versão do Android e do fabricante do dispositivo.

## Requisitos

- Flutter 3.35 ou superior
- Dart 3.9 ou superior
- Android SDK com API 35 ou superior
- JDK 17
- Android mínimo: API 24

## Como executar

```bash
flutter pub get
flutter run
```

Para gerar o APK release:

```bash
flutter build apk --release --no-tree-shake-icons
```

O arquivo será criado em:

```text
build/app/outputs/flutter-apk/app-release.apk
```

## Estrutura principal

```text
lib/main.dart                         Aplicação Flutter e telas principais
android/app/src/main/                 Manifesto, permissões e código Android
android/app/build.gradle.kts          Configuração de compilação Android
pubspec.yaml                          Dependências e metadados
README.md                             Documentação do projeto
```

## Dependências principais

- `archive`: criação e extração de ZIP
- `audioplayers`: reprodução de áudio
- `video_player`: reprodução de vídeo
- `encrypt`: criptografia AES
- `crypto`: derivação SHA-256
- `open_filex`: abertura com aplicativos externos
- `permission_handler`: permissões Android
- `share_plus`: compartilhamento
- `shared_preferences`: preferências e contas persistentes
- `webview_flutter`: prévia HTML

## Build atual

- Versão: `1.9.0`
- Código Android: `10`
- APK release: `build/app/outputs/flutter-apk/app-release.apk`

## Boas práticas para publicação

1. Não publique senhas de FTP no repositório.
2. Não inclua `build/` nem `.dart_tool/` no Git.
3. Revise o manifesto antes de distribuir uma versão em produção.
4. Use um keystore próprio para assinar versões distribuídas fora do ambiente de desenvolvimento.
5. Teste permissões e caminhos em diferentes versões do Android.

## Licença

Defina aqui a licença do projeto antes de publicar. Para software aberto, uma opção comum é MIT.
