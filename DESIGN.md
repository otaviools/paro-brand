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
  border-radius: var(--paro-raio-md);
  font-family: var(--paro-fonte);
  border: var(--paro-borda);
  padding: var(--paro-esp-4);
}
```

Para Tailwind v4, use `tokens/paro.tailwind.css`. Para outras ferramentas, `tokens/paro.json` segue o formato W3C Design Tokens.

---

## Escala tipográfica

| Uso | Tamanho | Peso Satoshi | Altura de linha |
|---|---|---|---|
| Título de página | 36 px | 700 Bold | 1.2 |
| Título de seção | 24 px | 700 Bold | 1.2 |
| Nome da rua | 18 px | 500 Medium | 1.4 |
| Corpo | 16 px | 400 Regular | 1.5 |
| Legenda, rótulo | 14 px | 400 Regular | 1.5 |
| Etiqueta caixa alta | 12 px | 700 Bold, tracking 0.18em | 1.4 |
| Percentual grande | 48 px | 900 Black | 1.0 |

Nunca centralize texto corrido. Máximo de 70 caracteres por linha em parágrafos.

---

## Espaçamento

Escala de 4 px: 4, 8, 12, 16, 24, 32, 48, 64. Nada fora dela.

Raio de borda: 8 px em botões e campos, 12 px em cards, 16 px no container do mapa. Full apenas em pílulas e badges.

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
