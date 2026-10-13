# Instruções para agentes de IA

Este arquivo define como usar a identidade visual do **Parô** ao gerar telas, apresentações, documentos ou qualquer material da marca.

Leia também o `README.md` e, quando o trabalho envolver interface, o `DESIGN.md`.

---

## Contexto do projeto

O Parô é um sistema que informa a **probabilidade de encontrar vaga** de estacionamento por rua e horário, no entorno da ESAMC Uberlândia e região central.

Ponto essencial: o Parô entrega **previsão**, não garantia. Nenhum texto, tela ou peça pode prometer que o usuário vai encontrar vaga. A promessa é informação antes do deslocamento.

---

## Regras absolutas

1. **Não redesenhe ativos.** Use os arquivos deste repositório. Não recrie o logotipo, o símbolo ou os grafismos, nem os reconstrua em código.
2. **Não altere as cores da marca.** Os valores do `tokens/paro.css` são a fonte da verdade.
3. **Ocupação de vaga é comunicada por rótulo e padrão, não por cor.** Use rótulo textual mais preenchimento — sólido, hachura diagonal, hachura densa ou tracejado. Não introduza cores fora da paleta da marca para representar ocupação.
4. **Não use emojis.** Para ícones, use a família [Lucide](https://lucide.dev/).
5. **Não prometa encontrar vaga.** Escreva sobre probabilidade, chance e previsão.
6. **Sempre exiba o horário da medição** ao mostrar dado de ocupação.

---

## Logotipo

| Situação                           | Arquivo                              |
| ---------------------------------- | ------------------------------------ |
| Fundo creme, claro ou branco       | `logo/logo-paro-fundo-claro.svg`     |
| Fundo asfalto, azul ou fotografia  | `logo/logo-paro-fundo-escuro.svg`    |
| Impressão em uma cor, fundo claro  | `logo/logo-monocromatica-preta.svg`  |
| Impressão em uma cor, fundo escuro | `logo/logo-monocromatica-branca.svg` |
| Avatar, ícone, cabeçalho compacto  | `simbolo/volante.svg`                |

Largura mínima de 120 px no digital. Abaixo disso, use o símbolo. Área livre de 2x ao redor, sendo x a altura do circunflexo.

Nunca rotacione, distorça, aplique sombra, contorno ou degradê.

---

## Cores

```
Creme       #FFF9E3   fundo de página, logotipo sobre foto
Céu         #C3D2D7   fundos amplos, respiro
Céu claro   #D2DEDA   superfícies, cards
Azul        #6EA8FF   volante, destaques
Azul texto  #3D74D6   quando o azul carrega texto
Concreto    #75746E   texto secundário
Asfalto     #32312C   textos, estrutura, fundos escuros
```

O creme e o asfalto são quentes de propósito. Não substitua por `#FFFFFF` nem por `#000000`.

Estados de ocupação, **exclusivos para dado real**, comunicados por rótulo textual mais padrão de preenchimento — nunca por cor:

```
Livre       até 60% de ocupação    preenchimento sólido + rótulo
Apertado    60% a 85%              hachura diagonal + rótulo
Lotado      acima de 85%          hachura densa + rótulo
Sem dado    trecho não medido     tracejado + rótulo
```

---

## Tipografia

**Manrope** é a família única: títulos, corpo, interface, tabelas. **JetBrains Mono** apenas para código e dados tabulares.

Para etiquetas e rótulos de canto, use Manrope Bold 11 px em caixa alta com `letter-spacing: 0.145em` (a classe `.paro-etiqueta`). Nunca aplique isso em texto corrido.

Carregamento pelo Google Fonts:

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Manrope:wght@300..800&display=swap"
  rel="stylesheet"
/>
```

Ou localmente, com `<link rel="stylesheet" href="fontes/fontes.css">` após baixar os arquivos conforme o `fontes/LEIAME.md`.

---

## Grafismos

| Arquivo               | Uso                                 |
| --------------------- | ----------------------------------- |
| `detalhe-1-malha`     | Fundo de seção, capa, textura ampla |
| `detalhe-2-isolinhas` | Capa, abertura de seção, densidade  |
| `detalhe-3-acento`    | Textura de fundo, papelaria         |
| `detalhe-4-radar`     | Carregamento, ícone de seção        |
| `detalhe-5-baias`     | Rodapé, divisor, cabeçalho          |

Um grafismo por tela. Grafismos de fundo entre 8% e 15% de opacidade. Nunca atrás de tabela ou texto corrido. Abaixo de 200 px de largura, o traço fino desaparece: aumente a espessura ou troque de grafismo.

Não crie grafismos novos a partir do símbolo.

---

## Tom de voz

Direto e prestativo, sem infantilizar. O usuário está com pressa.

- Escreva: "70% de chance de vaga às 19h"
- Não escreva: "Poxa, parece que tá difícil por aqui!"

Sempre exponha a incerteza. _Provavelmente cheio_ é honesto; _cheio_ é uma afirmação que os dados de campo não sustentam.

Frases aprovadas da marca: _Menos volta, mais vaga._ · _Chegue sabendo._ · _A gente não cria vagas. A gente mostra onde elas estão._

---

## Acessibilidade

Ocupação nunca é comunicada por cor. Cada estado se distingue por rótulo textual mais padrão de preenchimento — sólido, hachura diagonal, hachura densa ou tracejado. Isso também protege quem tem daltonismo, que afeta cerca de 8% dos homens.

Valide o contraste pela WCAG. O `Azul Parô` não alcança contraste suficiente para texto pequeno sobre creme: use `Azul texto` nesse caso.

---

## Dados pessoais

O projeto é acadêmico e trata de coleta com pessoas. Ao gerar formulários, telas ou materiais:

- Não crie campos para placa de veículo, CPF, nome completo ou telefone. Placa identifica indiretamente o titular e é dado pessoal sob a LGPD.
- Aplique minimização: só o campo necessário para a finalidade declarada.
- Em fotografias de veículos, borre as placas.
- Formulário de pesquisa e formulário de sorteio devem ser separados, para não vincular identidade às respostas.

---

## Exemplo de pedido bem formado

```
Crie a tela de resultado do Parô usando a identidade oficial.

Antes de começar, leia o README.md, o AGENTS.md e o DESIGN.md de:
https://github.com/otaviools/paro-brand

Use somente os arquivos oficiais do repositório e siga as regras de
logotipo, cores, tipografia, grafismos e acessibilidade.
```
