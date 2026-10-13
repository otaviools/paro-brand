# Fontes

Os arquivos de fonte **não estão versionados** neste repositório, por serem binários pesados.

## Manrope

Família única da marca. Pesos usados pelo Parô: Light 300, Regular 400, Medium 500, SemiBold 600, Bold 700 e ExtraBold 800. A versão variável cobre todos num único arquivo, de 200 a 800.

O `fontes.css` espera o arquivo `Manrope-Variable.woff2` nesta pasta. Para gerá-lo, baixe a fonte variável do repositório do Google Fonts e converta com o fontTools (`pip install fonttools brotli`):

```bash
curl -L -o Manrope-wght.ttf "https://github.com/google/fonts/raw/main/ofl/manrope/Manrope%5Bwght%5D.ttf"
python -c "from fontTools.ttLib import TTFont; f = TTFont('Manrope-wght.ttf'); f.flavor = 'woff2'; f.save('Manrope-Variable.woff2')"
```

Use a fonte completa, não um subconjunto latino: os subconjuntos deixam de fora a seta (→) usada nos horários das telas.

Para instalar no computador e usar em Figma, Canva ou PowerPoint, baixe os `.ttf` em https://fonts.google.com/specimen/Manrope

Licença SIL Open Font License 1.1: livre para uso pessoal e comercial.

## JetBrains Mono

Somente para código e dados tabulares. Baixe em https://www.jetbrains.com/lp/mono/

Licença SIL Open Font License 1.1.

## Alternativa sem download

Se preferir usar o CDN, ignore o `fontes.css` e use a tag `<link>` do Google Fonts indicada no README. A contrapartida é depender de conexão e de um domínio externo.
