# DESIGN.md

Orientações para construir interfaces do Parô. Complementa o `README.md` e o `AGENTS.md`.

---

## Princípio que organiza a interface

O Parô mostra **probabilidade**, não certeza. Toda decisão de design deve reforçar isso. Uma tela que parece dar uma resposta definitiva sobre algo incerto quebra a confiança na primeira vez que erra.

Na prática: exibir faixa em vez de número exato quando possível, mostrar sempre o horário da medição, e usar linguagem que admite incerteza.

---

## Tokens

Importe `tokens/paro.css` e use as variáveis. Não escreva valores hexadecimais direto no componente.

```css
@import url("tokens/paro.css");

.card-rua {
  background: var(--paro-superficie);
  border-radius: var(--paro-raio-card);
  font-family: var(--paro-fonte);
  border: var(--paro-borda);
  padding: var(--paro-esp-4);
}
```

Para Tailwind v4, use `tokens/paro.tailwind.css`. Para outras ferramentas, `tokens/paro.json` segue o formato W3C Design Tokens.

---

## Escala tipográfica

Valores das telas do Figma (Produto Mobile e Produto Desktop). Cada linha tem um token `--paro-texto-*` no `paro.css`.

| Uso | Tamanho | Peso Manrope | Token |
|---|---|---|---|
| Percentual de destaque (desktop) | 56 px | 800 ExtraBold | `--paro-texto-hero` |
| Percentual grande (mobile) | 48 px | 800 ExtraBold | `--paro-texto-percentual` |
| Indicador de painel | 40 px | 800 ExtraBold | `--paro-texto-kpi` |
| Número de card | 28 px | 800 ExtraBold | `--paro-texto-numero` |
| Título de página | 26 px | 700 Bold | `--paro-texto-titulo` |
| Número de stat, título de detalhe | 22 px | 800 ExtraBold ou 700 Bold | `--paro-texto-stat` |
| Botão principal (mobile) | 18 px | 700 Bold | `--paro-texto-botao` |
| Título de card, percentual de lista | 17 px | 700 Bold ou 800 ExtraBold | `--paro-texto-card` |
| Botão secundário, seletor de local | 16 px | 700 Bold ou 600 SemiBold | `--paro-texto-destaque` |
| Corpo, nome da rua na lista | 15 px | 500 Medium ou 700 Bold | `--paro-texto-corpo` |
| Menu, abas, campos | 14 px | 500 Medium | `--paro-texto-interface` |
| Subtítulo, legenda, badge | 13 px | 500 Medium ou 700 Bold | `--paro-texto-legenda` |
| Nota de rodapé, eixo de gráfico | 12 px | 400 Regular ou 500 Medium | `--paro-texto-nota` |
| Etiqueta caixa alta | 11 px | 700 Bold, tracking 0.145em | `--paro-texto-etiqueta` |
| Nome de rua no mapa | 10 px | 600 SemiBold | `--paro-texto-mapa` |

Nunca centralize texto corrido. Máximo de 70 caracteres por linha em parágrafos.

---

## Espaçamento

Escala de 4 px: 4, 8, 12, 16, 20, 24, 32, 48, 64. Nada fora dela.

Margem lateral de 24 px no mobile (frame de 393 px) e 32 px no desktop (frame de 1440 px). No desktop, barra lateral de 248 px e barra superior de 88 px; no mobile, barra de abas de 96 px.

| Raio | Onde | Token |
|---|---|---|
| 8 px | Badges, abas internas, padrões de ocupação | `--paro-raio-badge` |
| 10 px | Botões, campos, selects, itens de menu | `--paro-raio-botao` |
| 12 px | Alertas, stats, textareas | `--paro-raio-alerta` |
| 14 px | Card de lista de ruas | `--paro-raio-lista` |
| 16 px | Cards, hero e container do mapa | `--paro-raio-card` |
| full | Pílulas, switches e badge de status | `--paro-raio-full` |

Alturas de controle: botão principal de 56 px no mobile e 44 px no desktop, botão de ícone de 40 px, campo de 52 px no mobile e 40 px no desktop, abas de 40 px e badge de 28 px.

### Cores de produto

Além das cores de marca, as telas usam tons quentes derivados do creme e do asfalto. Ficam só na interface, nunca no logotipo, símbolo ou grafismos.

| Token | Claro | Escuro | Uso |
|---|---|---|---|
| `--paro-fundo` | `#FFF9E3` | `#32312C` | Fundo da página |
| `--paro-superficie` | `#FFFCF2` | `#3E3D37` | Cards, barra lateral, campos |
| `--paro-superficie-suave` | `#F3ECD4` | `#47463F` | Botão soft, stats, fundo de abas |
| `--paro-superficie-ativa` | `#D2DEDA` | `#4A5558` | Item ativo, badge soft, alerta |
| `--paro-texto-fraco` | `#75746E` | `#A8A69C` | Texto secundário |
| `--paro-texto-terciario` | `#8F8A7E` | `#9C998E` | Nomes de rua no mapa |
| `--paro-acao` | `#3D74D6` | `#6EA8FF` | Botão principal e links |
| `--paro-grafico-barra` | `#8CB0EE` | `#4F79BF` | Barras fora de destaque |
| `--paro-grafico-neutro` | `#D9D3C0` | `#4A4842` | Segmento neutro de gráfico |

O mapa tem cores próprias (`--paro-mapa-*`): fundo `#EEE7D2`, quadras `#E6DEC5`, praças `#DCE2D2`, vias `#FFFCF2` com contorno `#DDD3B7` e marcadores `#FFFDF5`. No tema escuro, todas mudam junto com os demais tokens.

O tema escuro vale pelo sistema ou por `data-tema="escuro"` na raiz do documento; `data-tema="claro"` força o claro.

### Padrões de ocupação em CSS

O `paro.css` traz as classes `.paro-padrao` e `.paro-padrao--livre`, `--apertado`, `--lotado` e `--sem-dado`, com os valores do Figma: hachura a 45° com traço de 1,2 px a cada 5 px (apertado) ou 2,8 px (lotado) e contorno tracejado 4/3 (sem dado). O Tailwind ganha as utilitárias `padrao-livre`, `padrao-apertado`, `padrao-lotado` e `padrao-sem-dado`. Sempre com o rótulo textual ao lado.

Sem sombras pesadas. Uma borda de 1 px em `--paro-borda` separa melhor e carrega mais rápido.

---

## Componentes

### Card de rua

Elemento central do produto. Contém:

- Nome da rua, 18 px Medium
- Faixa de status com padrão de preenchimento **e** rótulo
- Percentual em número grande, 48 px Black
- Horário da última medição, 14 px, cor `concreto`

O horário é obrigatório. Sem ele o usuário assume tempo real, e o Parô entrega previsão. Escrever "medido às 18h30" é honestidade de produto.

### Gráfico de ocupação por horário

Barras verticais por faixa de 30 minutos, diferenciadas por padrão de preenchimento, com linha tracejada em 85% marcando o limiar de dificuldade.

Eixo Y de 0% a 100%. Rotule o eixo — "taxa de ocupação" não é óbvio para quem chega direto pelo link.

### Seletor de dia

Pílulas horizontais de Seg a Sáb. A selecionada usa fundo `asfalto` com texto `creme`.

### Legenda

Sempre visível junto ao mapa, com os quatro padrões e os quatro rótulos. Não é opcional: sem ela o mapa é indecifrável para quem chega pela primeira vez.

### Estado vazio

Quando não há dado para o trecho, mostre `sem dado` com padrão tracejado e o texto "ainda não medimos esta rua". Nunca deixe o trecho em branco nem o marque como livre por omissão.

---

## Estados de ocupação

A ocupação é comunicada por rótulo textual mais padrão de preenchimento, não por cor.

| Estado | Ocupação | Padrão |
|---|---|---|
| Livre | até 60% | preenchimento sólido + rótulo |
| Apertado | 60% a 85% | hachura diagonal + rótulo |
| Lotado | acima de 85% | hachura densa + rótulo |
| Sem dado | — | tracejado + rótulo |

O corte em 85% vem do limiar em que, na literatura de mobilidade urbana, encontrar vaga passa a ser difícil na prática. É a mesma régua usada no protocolo de contagem em campo, então mapa e pesquisa falam a mesma língua.

O rótulo textual não é opcional: padrão de preenchimento sozinho não basta, e o par rótulo + padrão protege quem tem daltonismo.

---

## Duas camadas

**Camada de marca** — capa, slides, papelaria, cabeçalho, rodapé. Rigorosamente creme, céu, azul e asfalto.

**Camada de produto** — mapa, cards, gráficos. Mesma base, com os padrões de ocupação (sólido, hachura, tracejado) aplicados apenas onde há dado real.

Essa separação mantém a leitura limpa: o padrão de preenchimento só aparece onde carrega informação, nunca como decoração no institucional.

---

## Contraste

Valide pela WCAG. Combinações seguras:

| Texto | Fundo | Uso |
|---|---|---|
| `asfalto` | `creme` | corpo, títulos |
| `creme` | `asfalto` | modo escuro |
| `azul-texto` | `creme` | links, rótulos |
| `concreto` | `creme` | texto secundário |

O `azul` (`#6EA8FF`) funciona em logotipo, símbolo e áreas grandes, mas **não** em texto pequeno sobre creme. Use `azul-texto` nesses casos.

---

## Formulários

O projeto coleta dados de pessoas. Ao construir qualquer formulário:

- Sem campos de placa, CPF, nome completo ou telefone
- Consentimento como primeira pergunta, com opção de recusa que encerra o fluxo
- Faixa de renda sempre com opção "prefiro não informar"
- Formulário de pesquisa separado de formulário de sorteio

---

## Desempenho

Traço fino dos grafismos não sobrevive à redução. Abaixo de 200 px de largura, aumente a espessura ou troque de grafismo.

Prefira SVG a PNG em qualquer elemento da marca. Os PNGs existem para Canva, PowerPoint e ferramentas que não aceitam SVG.
