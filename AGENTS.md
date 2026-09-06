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
3. **Verde, âmbar e vermelho representam ocupação de vaga.** Nunca use essas cores como decoração, destaque genérico ou cor de marca.
4. **Não use emojis.** Para ícones, use a família [Lucide](https://lucide.dev/).
5. **Não prometa encontrar vaga.** Escreva sobre probabilidade, chance e previsão.
6. **Sempre exiba o horário da medição** ao mostrar dado de ocupação.

---

## Logotipo

| Situação | Arquivo |
|---|---|
| Fundo creme, claro ou branco | `logo/logo-paro-fundo-claro.svg` |
| Fundo asfalto, azul ou fotografia | `logo/logo-paro-fundo-escuro.svg` |
| Impressão em uma cor, fundo claro | `logo/logo-monocromatica-preta.svg` |
| Impressão em uma cor, fundo escuro | `logo/logo-monocromatica-branca.svg` |
| Avatar, ícone, cabeçalho compacto | `simbolo/volante.svg` |

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

Status de ocupação, **exclusivos para dado real**:

```
Livre       #00A86B   até 60% de ocupação
Apertado    #F0A020   60% a 85%
Lotado      #E03B3B   acima de 85%
Sem dado    #B4B2A8   trecho não medido
```

O creme e o asfalto são quentes de propósito. Não substitua por `#FFFFFF` nem por `#000000`.

---

## Tipografia

**Satoshi** é a família única: títulos, corpo, interface, tabelas. **JetBrains Mono** apenas para código e dados tabulares.

Para etiquetas e rótulos de canto, use Satoshi Bold em caixa alta com `letter-spacing: 0.18em`. Nunca aplique isso em texto corrido.

Carregamento via CDN:

```html
<link rel="preconnect" href="https://api.fontshare.com">
<link href="https://api.fontshare.com/v2/css?f[]=satoshi@300,400,500,700,900&display=swap" rel="stylesheet">
```

Ou localmente, com `<link rel="stylesheet" href="fontes/fontes.css">` após baixar os arquivos conforme o `fontes/LEIAME.md`.

---

## Grafismos

| Arquivo | Uso |
|---|---|
| `detalhe-1-malha` | Fundo de seção, capa, textura ampla |
| `detalhe-2-isolinhas` | Capa, abertura de seção, densidade |
| `detalhe-3-acento` | Textura de fundo, papelaria |
| `detalhe-4-radar` | Carregamento, ícone de seção |
| `detalhe-5-baias` | Rodapé, divisor, cabeçalho |

Um grafismo por tela. Grafismos de fundo entre 8% e 15% de opacidade. Nunca atrás de tabela ou texto corrido. Abaixo de 200 px de largura, o traço fino desaparece: aumente a espessura ou troque de grafismo.

Não crie grafismos novos a partir do símbolo.

---

## Tom de voz

Direto e prestativo, sem infantilizar. O usuário está com pressa.

- Escreva: "70% de chance de vaga às 19h"
- Não escreva: "Poxa, parece que tá difícil por aqui!"

Sempre exponha a incerteza. *Provavelmente cheio* é honesto; *cheio* é uma afirmação que os dados de campo não sustentam.

Frases aprovadas da marca: *Menos volta, mais vaga.* · *Chegue sabendo.* · *A gente não cria vagas. A gente mostra onde elas estão.*

---

## Acessibilidade

Status nunca é comunicado só por cor. Verde, âmbar e vermelho juntos são o pior caso para daltonismo, que afeta cerca de 8% dos homens. Cada estado precisa de um segundo sinal: preenchimento sólido, hachura diagonal, hachura densa ou tracejado, sempre com rótulo textual.

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
https://github.com/SEU-USUARIO/paro-brand

Use somente os arquivos oficiais do repositório e siga as regras de
logotipo, cores, tipografia, grafismos e acessibilidade.
```
