![Parô](logo/logo-paro-fundo-escuro.svg)

# Marca Parô

Repositório oficial da identidade visual do **Parô** — sistema que informa a probabilidade de encontrar vaga de estacionamento por rua e horário, no entorno da ESAMC Uberlândia e região central.

Aqui você encontra logotipo, símbolo, favicons, grafismos, fontes, tokens de design e as orientações para aplicar a marca em materiais, interfaces e projetos de código.

> Use sempre os arquivos originais deste repositório. Não redesenhe, recorte, recolore ou reconstrua a marca.

**Assinatura:** _Menos volta, mais vaga._
**Linha de apoio:** Mostramos a chance de vaga em cada rua, por horário.

---

## Por onde começar

| O que você precisa fazer | Comece por                                                                                  |
| ------------------------ | ------------------------------------------------------------------------------------------- |
| Baixar o logotipo        | Seção [Logotipo](#logotipo)                                                                 |
| Criar uma interface      | [Tokens de design](#tokens-de-design), [Tipografia](#tipografia) e o [DESIGN.md](DESIGN.md) |
| Montar slides ou capa    | [Grafismos](#grafismos) e [Cores](#cores)                                                   |
| Orientar um agente de IA | Peça para ele ler o [AGENTS.md](AGENTS.md) antes de começar                                 |
| Entender o produto       | Seção [O que o Parô promete](#o-que-o-parô-promete)                                         |

---

## O que o Parô promete

O Parô entrega **previsão**, não garantia. A promessa é informação antes do deslocamento, calculada sobre observação de campo.

Nenhum texto, tela ou peça pode prometer que o usuário vai encontrar vaga. Frases como _sua vaga te espera_ ou _nunca mais procure vaga_ soam melhor e são indefensáveis.

Essa restrição orienta o design inteiro: exibir faixa em vez de número exato, mostrar sempre o horário da medição, e usar linguagem que admite incerteza.

---

## Logotipo

O logotipo é a palavra `parô` em construção geométrica caixa baixa, com o `o` substituído por um volante e o circunflexo acima. A descendente do `p` forma uma cauda curva — é o único desvio da geometria e o que dá personalidade à marca.

| Versão                                                                                                      | Quando usar                         | Arquivos                                                                              |
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------- | ------------------------------------------------------------------------------------- |
| [![Logo Parô fundo claro](logo/logo-paro-fundo-claro.svg)](logo/logo-paro-fundo-claro.svg)                  | Fundos creme, claros ou brancos     | [svg](logo/logo-paro-fundo-claro.svg) · [png](logo/logo-paro-fundo-claro.png)         |
| [![Logo Parô fundo escuro](logo/logo-paro-fundo-escuro.svg)](logo/logo-paro-fundo-escuro.svg)               | Fundos asfalto, azul ou fotografias | [svg](logo/logo-paro-fundo-escuro.svg) · [png](logo/logo-paro-fundo-escuro.png)       |
| [![Logo Parô monocromática preta](logo/logo-monocromatica-preta.svg)](logo/logo-monocromatica-preta.svg)    | Uma cor sobre fundo claro           | [svg](logo/logo-monocromatica-preta.svg) · [png](logo/logo-monocromatica-preta.png)   |
| [![Logo Parô monocromática branca](logo/logo-monocromatica-branca.svg)](logo/logo-monocromatica-branca.svg) | Uma cor sobre fundo escuro          | [svg](logo/logo-monocromatica-branca.svg) · [png](logo/logo-monocromatica-branca.png) |

Nas versões monocromáticas o volante perde definição, porque é o azul que o separa do resto da palavra. Reserve-as para carimbo e impressão em uma cor.

### Cuidados importantes

- Largura mínima de **120 px** no digital ou **2 cm** no impresso. Abaixo disso, use o símbolo.
- Mantenha área livre de **2x** ao redor, sendo x a altura do circunflexo.
- Não altere cores, proporções, tipografia ou espaçamento.
- Não rotacione, distorça, nem aplique sombra, contorno ou degradê.
- O volante é sempre azul nas versões coloridas. Nunca o recolora fora da paleta da marca.

### Símbolo

[![Símbolo Parô](simbolo/volante.svg)](simbolo/volante.svg)

O volante com o circunflexo é a versão reduzida da marca. Use em avatar, ícone de aplicativo, cabeçalho compacto e marca d'água.

| Versão  | Quando usar                    | Arquivos                                                                |
| ------- | ------------------------------ | ----------------------------------------------------------------------- |
| Azul    | Padrão, sobre creme ou asfalto | [svg](simbolo/volante.svg) · [png](simbolo/volante.png)                 |
| Asfalto | Uma cor sobre fundo claro      | [svg](simbolo/volante-asfalto.svg) · [png](simbolo/volante-asfalto.png) |
| Creme   | Uma cor sobre fundo escuro     | [svg](simbolo/volante-creme.svg) · [png](simbolo/volante-creme.png)     |

O símbolo não substitui o logotipo completo em capas, slides de abertura ou no relatório.

---

## Favicons

O símbolo oficial encaixado em área quadrada de 64 px, com respiro proporcional.

### Sites e ferramentas menores

| Visual                                                                     | Arquivo       | Característica    | Formatos                                                        |
| -------------------------------------------------------------------------- | ------------- | ----------------- | --------------------------------------------------------------- |
| [![Favicon principal](favicon/favicon.svg)](favicon/favicon.svg)           | `favicon`     | Símbolo sem fundo | [svg](favicon/favicon.svg) · [png](favicon/favicon.png)         |
| [![Favicon alternativo](favicon/favicon-alt.svg)](favicon/favicon-alt.svg) | `favicon-alt` | Squircle azul     | [svg](favicon/favicon-alt.svg) · [png](favicon/favicon-alt.png) |

### Aplicações com vários ambientes

As diferenças de cor ajudam a identificar rapidamente se a aba aberta é de produção, homologação ou desenvolvimento local.

| Ambiente    | Visual                                                                               | Arquivo             | Formatos                                                                    |
| ----------- | ------------------------------------------------------------------------------------ | ------------------- | --------------------------------------------------------------------------- |
| Produção    | [![Favicon produção](favicon/favicon-producao.svg)](favicon/favicon-producao.svg)    | `favicon-producao`  | [svg](favicon/favicon-producao.svg) · [png](favicon/favicon-producao.png)   |
| Homologação | [![Favicon homologação](favicon/favicon-homolog.svg)](favicon/favicon-homolog.svg)   | `favicon-homolog`   | [svg](favicon/favicon-homolog.svg) · [png](favicon/favicon-homolog.png)     |
| Localhost   | [![Favicon localhost](favicon/favicon-localhost.svg)](favicon/favicon-localhost.svg) | `favicon-localhost` | [svg](favicon/favicon-localhost.svg) · [png](favicon/favicon-localhost.png) |

---

## Grafismos

Os grafismos da pasta [grafismos/](grafismos) são desenhados em traço fino, entre 1,3 e 2,6 px, com vocabulário de cartografia. Em todos, o azul marca exatamente um ponto de interesse — o resto é estrutura neutra.

Cada arquivo tem variante para fundo claro e escuro, em `svg` e `png`.

| Grafismo              | O que é                                              | Onde usar                           | Exemplo                                              |
| --------------------- | ---------------------------------------------------- | ----------------------------------- | ---------------------------------------------------- |
| `detalhe-1-malha`     | Grade de ruas levemente irregular, um trecho em azul | Fundo de seção, capa, textura ampla | [ver](docs/previews/preview-detalhe-1-malha.svg)     |
| `detalhe-2-isolinhas` | Curvas de nível de ocupação, núcleo em azul          | Capa, abertura de seção, densidade  | [ver](docs/previews/preview-detalhe-2-isolinhas.svg) |
| `detalhe-3-acento`    | Circunflexo da marca vazado, em repetição esparsa    | Textura de fundo, papelaria         | [ver](docs/previews/preview-detalhe-3-acento.svg)    |
| `detalhe-4-radar`     | Anéis concêntricos com marcas radiais e ponteiro     | Carregamento, ícone de seção        | [ver](docs/previews/preview-detalhe-4-radar.svg)     |
| `detalhe-5-baias`     | Baias de estacionamento em contorno, uma em azul     | Rodapé, divisor, cabeçalho          | [ver](docs/previews/preview-detalhe-5-baias.svg)     |

### Regras de aplicação

- **Um grafismo por tela.** Dois competindo viram poluição.
- Grafismos de fundo (`detalhe-1`, `detalhe-3`) sempre entre **8% e 15% de opacidade**.
- Traço fino não sobrevive à redução. Abaixo de 200 px de largura, aumente a espessura ou troque de grafismo.
- Nunca atrás de tabela ou texto corrido. Só em capas, cabeçalhos, rodapés e áreas de respiro.
- Não crie novos grafismos nem rotacione os existentes.

---

## Cores

A paleta vem da capa oficial do projeto.

### Marca

| Cor        | HEX       | RGB             | Uso                                  |
| ---------- | --------- | --------------- | ------------------------------------ |
| Creme Parô | `#FFF9E3` | `255, 249, 227` | Logotipo sobre foto, fundo de página |
| Céu Parô   | `#C3D2D7` | `195, 210, 215` | Fundos amplos, áreas de respiro      |
| Céu claro  | `#D2DEDA` | `210, 222, 218` | Superfícies secundárias, cards       |
| Céu escuro | `#BAC7CD` | `186, 199, 205` | Bordas suaves, separadores           |
| Azul Parô  | `#6EA8FF` | `110, 168, 255` | Volante, destaques, direção do olhar |
| Azul texto | `#3D74D6` | `61, 116, 214`  | Quando o azul precisa carregar texto |
| Concreto   | `#75746E` | `117, 116, 110` | Texto secundário, legendas           |
| Asfalto    | `#32312C` | `50, 49, 44`    | Textos, estrutura, fundos escuros    |

O creme e o asfalto são quentes de propósito: `#FFF9E3` puxa para o amarelo e `#32312C` tem base marrom, não cinza neutro. É o que dá o ar analógico da capa. Não substitua por branco puro nem por preto puro.

### Estados de ocupação

A ocupação de vaga é comunicada por rótulo textual mais padrão de preenchimento, **não por cor**. Só aparece onde há dado real.

| Estado   | Ocupação     | Padrão                        | Significado           |
| -------- | ------------ | ----------------------------- | --------------------- |
| Livre    | até 60%      | preenchimento sólido + rótulo | Boa chance de vaga    |
| Apertado | 60% a 85%    | hachura diagonal + rótulo     | Vai precisar procurar |
| Lotado   | acima de 85% | hachura densa + rótulo        | Considere alternativa |
| Sem dado | —            | tracejado + rótulo            | Trecho não medido     |

O corte em 85% não é arbitrário: é o limiar em que, na literatura de mobilidade urbana, encontrar vaga passa a ser difícil na prática. É a mesma régua do protocolo de contagem em campo, então mapa e pesquisa falam a mesma língua.

### Duas regras que não podem ser quebradas

**A ocupação nunca é representada por cor.** Cada estado se distingue por rótulo e padrão de preenchimento. Assim a cor não compete com a informação, e não há dúvida sobre o que um tom na tela significa.

**Cada estado precisa de rótulo textual.** Padrão de preenchimento sozinho não basta: sólido, hachura diagonal, hachura densa e tracejado sempre acompanham o rótulo escrito. Isso também protege quem tem daltonismo, que afeta cerca de 8% dos homens.

Em produtos digitais, valide o contraste pela WCAG. O `Azul Parô` funciona no logotipo, no símbolo e em áreas grandes, mas não alcança contraste suficiente para texto pequeno sobre creme — use `Azul texto` nesses casos.

---

## Tipografia

| Família            | Uso                                                                                                                                                                      |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Satoshi**        | Família única da marca: títulos, chamadas, parágrafos, interface, tabelas e formulários. Grotesca de construção geométrica, em diálogo direto com o desenho do logotipo. |
| **JetBrains Mono** | Código, comandos, logs e dados monoespaçados.                                                                                                                            |

Não use JetBrains Mono em títulos ou texto corrido.

### Pesos

| Peso        | Quando usar                                                |
| ----------- | ---------------------------------------------------------- |
| Light 300   | Subtítulos grandes, em fundo limpo. Evite abaixo de 18 px. |
| Regular 400 | Corpo, legendas, rótulos                                   |
| Medium 500  | Nome de rua, ênfase leve, itens de menu                    |
| Bold 700    | Títulos, botões, etiquetas em caixa alta                   |
| Black 900   | Apenas percentuais grandes e números de destaque           |

### Escala

| Uso                 | Tamanho | Peso                      | Altura de linha |
| ------------------- | ------- | ------------------------- | --------------- |
| Título de página    | 36 px   | 700 Bold                  | 1.2             |
| Título de seção     | 24 px   | 700 Bold                  | 1.2             |
| Nome da rua         | 18 px   | 500 Medium                | 1.4             |
| Corpo               | 16 px   | 400 Regular               | 1.5             |
| Legenda, rótulo     | 14 px   | 400 Regular               | 1.5             |
| Etiqueta caixa alta | 12 px   | 700 Bold, tracking 0.18em | 1.4             |
| Percentual grande   | 48 px   | 900 Black                 | 1.0             |

Nunca centralize texto corrido. Máximo de 70 caracteres por linha em parágrafos.

### Etiquetas

A capa usa caixa alta com entreletra bem aberta nas frases de canto. Esse tratamento é um recurso da marca, não uma fonte diferente: Satoshi Bold, `text-transform: uppercase`, `letter-spacing: 0.18em`, corpo pequeno.

```css
.paro-etiqueta {
  font-family: "Satoshi", sans-serif;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.18em;
  font-size: 0.75rem;
}
```

Reserve para etiquetas, rótulos de canto e chamadas curtas. Nunca em texto corrido — entreletra aberta destrói a legibilidade em parágrafo.

### Como usar as fontes

**Opção 1 — CDN da Fontshare.** Mais simples, requer internet:

```html
<link rel="preconnect" href="https://api.fontshare.com" />
<link
  href="https://api.fontshare.com/v2/css?f[]=satoshi@300,400,500,700,900&display=swap"
  rel="stylesheet"
/>
```

**Opção 2 — arquivos locais.** Recomendado para o protótipo, funciona offline:

```html
<link rel="stylesheet" href="fontes/fontes.css" />
```

Os arquivos de fonte **não estão versionados** aqui, por serem binários pesados e de licenciamento de terceiros. Baixe em [fontshare.com/fonts/satoshi](https://www.fontshare.com/fonts/satoshi) e coloque os `.woff2` na pasta [fontes/](fontes) — o `fontes.css` já os referencia. Instruções completas em [fontes/LEIAME.md](fontes/LEIAME.md).

Para instalar no computador e usar em Figma, Canva ou PowerPoint, baixe também os `.otf` ou `.ttf`.

Evite pesos leves em tamanhos pequenos, fundos complexos ou baixa resolução.

---

## Tokens de design

A pasta [tokens/](tokens) reúne cores, fontes, espaçamentos, raios e limiares usados em interfaces.

| Arquivo                                       | Uso                                     |
| --------------------------------------------- | --------------------------------------- |
| [paro.css](tokens/paro.css)                   | Variáveis CSS prontas para projetos web |
| [paro.json](tokens/paro.json)                 | Tokens no formato W3C Design Tokens     |
| [paro.tailwind.css](tokens/paro.tailwind.css) | Bloco `@theme` para Tailwind CSS v4     |

Exemplo com CSS:

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

Para orientações completas sobre componentes, contraste e hierarquia visual, consulte o [DESIGN.md](DESIGN.md).

---

## Componentes do produto

**Card de rua** — nome da rua, faixa de status com padrão de preenchimento e rótulo, percentual em número grande, e **horário da última medição**. O horário é obrigatório: sem ele o usuário assume tempo real, e o Parô entrega previsão.

**Gráfico de ocupação por horário** — barras verticais por faixa de 30 minutos, diferenciadas por padrão de preenchimento, com linha tracejada em 85% marcando o limiar de dificuldade.

**Legenda** — sempre visível junto ao mapa, com os quatro padrões e os quatro rótulos. Não é opcional.

**Estado vazio** — quando não há dado, mostre `sem dado` com padrão tracejado e o texto "ainda não medimos esta rua". Nunca deixe em branco nem marque como livre por omissão.

---

## Duas camadas

**Camada de marca** — capa, slides, papelaria, cabeçalho, rodapé. Rigorosamente creme, céu, azul e asfalto.

**Camada de produto** — mapa, cards, gráficos. Mesma base, com os padrões de ocupação (sólido, hachura, tracejado) aplicados apenas onde há dado real.

Essa separação mantém a leitura limpa: o padrão de preenchimento só aparece onde carrega informação, nunca como decoração no institucional.

---

## Tom de voz

Direto e prestativo, sem infantilizar. O usuário está com pressa.

- Diga: "70% de chance de vaga às 19h"
- Não diga: "Poxa, parece que tá difícil por aqui!"

Sempre exponha a incerteza. _Provavelmente cheio_ é honesto. _Cheio_ é uma afirmação que os dados de campo não sustentam.

### Frases aprovadas

| Frase                                                     | Onde usar                                    |
| --------------------------------------------------------- | -------------------------------------------- |
| _Menos volta, mais vaga._                                 | Assinatura de capa, dividida entre os cantos |
| _Chegue sabendo._                                         | Assinatura curta ao lado do logotipo         |
| _Todo mundo já rodou o quarteirão. Ninguém precisava._    | Frase de capa, rodapé                        |
| _A gente não cria vagas. A gente mostra onde elas estão._ | Abertura do manual, primeira página interna  |

Não use emojis. Para ícones, use a família [Lucide](https://lucide.dev/).

---

## Uso com agentes de IA

Antes de pedir que um agente crie uma tela, apresentação ou documento do Parô, envie o link deste repositório e peça para ele consultar:

1. [README.md](README.md)
2. [AGENTS.md](AGENTS.md)
3. [DESIGN.md](DESIGN.md), quando o trabalho envolver interfaces

O `AGENTS.md` explica como usar logotipos, favicons, grafismos, fontes e demais ativos. O `DESIGN.md` reúne os tokens e as orientações específicas para produtos digitais.

O arquivo `CLAUDE.md` aponta para o `AGENTS.md`, permitindo que o Claude Code encontre as mesmas instruções.

Exemplo de pedido:

```
Crie a tela de resultado do Parô usando a identidade visual oficial.

Antes de começar, leia o README.md, o AGENTS.md e o DESIGN.md de:
https://github.com/SEU-USUARIO/paro-brand

Use somente os arquivos oficiais do repositório e siga as regras de
logotipo, cores, tipografia, grafismos e acessibilidade.
```

As mesmas regras valem para pessoas e agentes:

- Não use emojis. Use ícones da família [Lucide](https://lucide.dev/).
- Para logos de terceiros, procure no [Iconify](https://icon-sets.iconify.design/) ou no [Icônes](https://icones.js.org/).
- Não redesenhe ativos existentes.
- Use o azul como destaque. Não introduza cores fora da paleta da marca.
- Valide o contraste em materiais digitais.
- Nenhum texto promete encontrar vaga.

---

## Dados pessoais e LGPD

O projeto coleta dados de pessoas em pesquisa de campo. Ao criar formulários, telas ou materiais:

- Sem campos de placa de veículo, CPF, nome completo ou telefone. Placa identifica indiretamente o titular e é dado pessoal sob a Lei 13.709/2018.
- Aplique minimização: só o campo necessário para a finalidade declarada.
- Faixa de renda sempre com opção "prefiro não informar".
- Formulário de pesquisa separado de formulário de sorteio, para não vincular identidade às respostas.
- Em fotografias de veículos, borre as placas.

---

## Estrutura do repositório

```
paro-brand/
├── README.md          este documento
├── AGENTS.md          regras para agentes de IA
├── CLAUDE.md          direcionamento para o AGENTS.md
├── DESIGN.md          tokens e orientações para interfaces
├── LICENCA.md         licença de uso da marca em português
├── LICENSE.md         licença de uso da marca em inglês
├── docs/              paleta e previews de aplicação
├── favicon/           favicons comuns e por ambiente
├── fontes/            fontes.css e instruções de download
├── grafismos/         cinco grafismos, claro e escuro
├── logo/              logotipo em quatro versões
├── mascote/           Vaguinha em quatro expressões
├── simbolo/           volante isolado
└── tokens/            tokens CSS, JSON e Tailwind CSS v4
```

---

## Licença

© Parô. Trabalho acadêmico da disciplina de Pesquisa de Mercado, ESAMC Uberlândia.

Este repositório é público para facilitar o acesso da equipe, de professores e de avaliadores. Isso não significa que os ativos sejam de uso livre.

Termos completos em [LICENCA.md](LICENCA.md), em português, e [LICENSE.md](LICENSE.md), em inglês.

As fontes são de terceiros: **Satoshi** pertence à Indian Type Foundry e é distribuída pela [Fontshare](https://www.fontshare.com/fonts/satoshi); **JetBrains Mono** usa a [SIL Open Font License 1.1](https://openfontlicense.org/).
