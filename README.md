# Caderno do Professor Adjunto I — site HTML + PWA

Site estático para estudos, questões, simulados, redação e revisão. Não exige Node.js, banco de dados ou servidor de aplicação.

## Arquivos de publicação

- `index.html`: página principal, estilos e lógica da aplicação.
- `manifest.webmanifest`: metadados de instalação PWA.
- `service-worker.js`: cache do shell para acesso offline.
- `icon.svg`: ícone vetorial do aplicativo.
- `.nojekyll`: evita processamento Jekyll pelo GitHub Pages.

## Publicar gratuitamente no GitHub Pages

1. Revise a branch `feat/pwa-mobile-estudos-20261012` e faça merge na `main` **somente após testes e autorização**.
2. No GitHub, abra o repositório > **Settings** > **Pages**.
3. Em **Build and deployment**, escolha **Deploy from a branch**, `main`, pasta `/(root)` e salve.
4. Acesse: https://osakasp.github.io/caderno-professor-adjunto-ibam/
5. No Chrome Android, use menu > **Instalar app** ou **Adicionar à tela inicial**, quando disponível.

O acesso HTTPS é necessário para o service worker. Instalação depende da compatibilidade do navegador. No iPhone, use Safari > Compartilhar > Adicionar à Tela de Início.

## Atenção aos dados

Respostas, histórico de erros e redações são guardados em `localStorage`, no navegador/dispositivo usado. Trocar de domínio cria outro armazenamento; **o progresso não migra automaticamente**. Não limpe dados do navegador antes de fazer uma cópia. Os arquivos desta branch não alteram dados do site publicado.

## Testes necessários antes de publicar

- Abrir `index.html` via HTTPS em Android, iPhone e desktop.
- Responder questões, recarregar a página e verificar persistência.
- Verificar simulados, filtros, caderno de erros, revisão, redação e exportação PNG.
- Confirmar instalação PWA e disponibilidade offline após primeira visita online.
- Confirmar que não existem falhas no console nem erros de recursos.
