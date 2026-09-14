# Molduras ABaC

Site estático para aplicar molduras da Associação Bahia Central sobre a câmera do celular.

## Moldura inicial
Semana do Lenço 2026

ID:
`semana-do-lenco-2026`

TOKEN:
`_x1q-mlnIH0QNkrrPdjHtg`

Após publicar, a URL privada terá este formato:

`https://SEU-USUARIO.github.io/SEU-REPOSITORIO/?f=semana-do-lenco-2026&k=_x1q-mlnIH0QNkrrPdjHtg`

Esse é o endereço que deve virar QR Code.

## Como funciona
- A página inicial, sem parâmetros, NÃO mostra nenhuma moldura.
- Cada moldura exige ID + token correto.
- `robots.txt` e `noindex` evitam indexação normal em buscadores.
- A moldura pode ter data inicial/final no `frames.json`.
- A foto final é composta em 1080 × 1920 px.
- O usuário pode compartilhar pelo menu nativo do celular ou salvar.

## Atenção sobre privacidade do link
Isto reduz muito a descoberta casual, mas não é segurança absoluta:
qualquer pessoa que receba o QR Code ou compartilhe a URL poderá abrir a moldura.
Para controle forte de acesso seria necessário um backend/autenticação.

## Publicação gratuita no GitHub Pages
1. Crie um repositório, por exemplo `molduras-abac`.
2. Envie todo o conteúdo desta pasta para a raiz do repositório.
3. Em Settings > Pages, escolha Deploy from a branch.
4. Selecione a branch `main` e pasta `/root`.
5. Aguarde o GitHub informar a URL HTTPS.
6. Substitua `SEU-USUARIO/SEU-REPOSITORIO` na URL acima pela URL publicada.
7. Gere o QR Code usando a URL completa com `?f=...&k=...`.

## Adicionar novas molduras
1. Coloque um novo PNG Alpha 1080 × 1920 dentro de `assets/`.
2. Abra `admin.html` localmente para gerar um novo ID/token.
3. Copie o objeto gerado para o array `frames` em `frames.json`.
4. Publique a atualização.
5. Gere um QR Code específico para essa nova URL.

## Requisito de câmera
A API de câmera do navegador exige HTTPS. GitHub Pages usa HTTPS e funciona bem para isso.
