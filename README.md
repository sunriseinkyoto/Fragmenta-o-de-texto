# Fragmentador de Texto

Solução em Python para dividir textos longos em blocos menores e organizados. Por padrão fatia em trechos de 1000 caracteres e gera metadados de rastreio para cada pedaço. Também lê o texto bruto a partir de PDF.

## Requisitos

- Python 3.8+
- `PyPDF2` (`pip install PyPDF2`)

## Como funciona

- **Leitura de PDF:** extrai texto de todas as páginas
- **Fatiamento:** divide o texto bruto em pedaços com tamanho configurável
- **Metadados:** cada pedaço inclui índice e posições de início/fim no texto original

## Uso

```python
from caracteres import ler_pdf, fragmentar_texto

texto = ler_pdf(r"caminho\para\arquivo.pdf")
fragmentos = fragmentar_texto(texto, tamanho_fragmento=1000)

for item in fragmentos:
    print(item["indice_fragmento"], item["inicio"], item["fim"])
    print(item["fragmento"])
```

## Arquivos

- `caracteres.py` — leitura de PDF e lógica de fragmentação
- `README.md` — este guia

## Autor

Matheus Coutinho ([@sunriseinkyoto](https://github.com/sunriseinkyoto))
