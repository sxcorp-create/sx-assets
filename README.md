# SX Corp — artes da assinatura de e-mail

Repositório **público de propósito**. Ele hospeda, via GitHub Pages, as imagens que
aparecem na assinatura de e-mail da SX Corp — as mesmas que saem em toda mensagem
que a empresa envia. Não há nada aqui que já não seja público.

## Por que existe

As artes eram servidas pelo próprio SX Flow. Imagem de assinatura tem vida longa —
fica citada no histórico de toda resposta de uma thread — mas o Flow reinicia várias
vezes por dia a cada deploy. Quando o proxy de imagem do destinatário busca a imagem
justamente nessa janela, ele recebe erro **e guarda o erro**: a logo desaparece
daquela cópia da mensagem para sempre. Foi o que aconteceu em 27/08/2026, numa
thread com o TJMG.

O GitHub Pages tira a imagem desse caminho crítico: é CDN, não reinicia junto com a
aplicação.

## Arquivos

| Arquivo | Onde aparece |
| --- | --- |
| `logo-navy-v6.png` | assinatura padrão (templates light, hub, marketing, compact, tmc) |
| `logo-titanium-v6.png` | Titanium — 10 Anos (comercial e financeiro) |
| `logo-tech-v6.png` | template Tecnologia (`tecnologia@`) |
| `banner-10anos-v6.png` | banner de campanha do template Marketing |

## Regras

**O sufixo `-vN` faz parte do contrato.** Arte nova nunca substitui um arquivo
existente: entra com o número seguinte, e o `ASSET_VER` do SX Flow é incrementado
junto (`src/routes/signature.js`). Sobrescrever um arquivo publicado quebraria a
logo de todo e-mail já enviado que aponta para ele.

Os arquivos apontados por assinaturas antigas ficam aqui **para sempre**, mesmo
depois de saírem de uso.

Fonte das artes: `public/signature/` no repositório `sx-flow`.
