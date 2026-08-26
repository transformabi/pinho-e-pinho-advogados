# Pinho & Pinho Advogados

Proposta de site para o escritório [Pinho & Pinho Advogados](https://www.pinhoepinho.adv.br/),
especializado em direito previdenciário no Rio de Janeiro.

Site de página única, construído em HTML, CSS e JavaScript puros. Sem framework,
sem etapa de build, sem dependência instalada. São dois arquivos e uma pasta de imagens.

## Como ver

Qualquer servidor estático serve a pasta como está:

```bash
npx http-server . -p 8123
```

Depois abra `http://localhost:8123`.

Abrir o `index.html` com dois cliques também funciona, mas o navegador bloqueia
o carregamento do vídeo em endereços `file://`, então a abertura aparece na
versão de imagem fixa. É um estado previsto no projeto, não uma falha.

## O que tem dentro

- **Abertura cinematográfica** conduzida pela rolagem: o vídeo avança conforme
  a pessoa desce a página e recua quando ela sobe. Em celulares, tablets em pé
  e para quem pede movimento reduzido, entra uma imagem fixa composta, e o
  vídeo não chega nem a ser baixado.
- **13 áreas de atuação** com as descrições técnicas do próprio escritório.
- **Linha do tempo interativa**: segure o botão e os anos de contribuição
  acendem um a um.
- **Três endereços** com CEP e link direto para o mapa.
- **WhatsApp como ação única**, presente no topo o tempo todo.

## Desempenho

Medido com o navegador simulando um celular sem cache, como um visitante novo:

| | Internet boa (4G) | Internet fraca |
|---|---|---|
| Página carregada | 1,19 s | 1,49 s |
| Peso | 105 KB | 105 KB |
| Arquivos baixados | 5 | 5 |

## Acessibilidade e robustez

- Contraste do texto sobre a abertura medido entre 6,5:1 e 9,5:1, contra um piso de 3,5:1.
- `prefers-reduced-motion` respeitado nos dois sentidos, inclusive quando a
  preferência muda com a página já aberta.
- Marcos semânticos, hierarquia de títulos, link para pular ao conteúdo,
  foco visível e alvos de toque de 44px.
- A página fica completa e legível mesmo se o vídeo nunca carregar.

## Estado atual

O vídeo de abertura ainda não foi gerado. Enquanto isso, a abertura usa um
amanhecer desenhado em CSS, que é um estado projetado e não um espaço vazio.
Os arquivos `assets/hero-scrub.mp4`, `assets/hero-poster.jpg` e
`assets/hero-ending.jpg` entram depois, sem nenhuma outra alteração no código.

## Créditos

O logotipo e as fotos dos escritórios pertencem à Pinho & Pinho Advogados.
Tipografia: Marcellus, Source Sans 3 e IBM Plex Mono, via Google Fonts.
