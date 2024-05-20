# Criando-uma-Biblioteca-de-Utilidades

Vamos criar uma biblioteca de utilidades em Python, que é uma linguagem de programação excelente para esse tipo de projeto devido à sua legibilidade e simplicidade. A biblioteca será modularizada, o que significa que cada funcionalidade será separada em seu próprio módulo para manter o código organizado e fácil de manter.

### Estrutura da Biblioteca
A estrutura básica da biblioteca pode ser assim:

```
biblioteca_de_utilidades/
|-- __init__.py
|-- matematica.py
|-- texto.py
|-- data.py
```

- `__init__.py`: Este arquivo torna o diretório uma biblioteca Python.
- `matematica.py`: Módulo para funções matemáticas úteis.
- `texto.py`: Módulo para manipulação e análise de texto.
- `data.py`: Módulo para trabalhar com datas e horários.

### Exemplos de Código

Aqui estão alguns exemplos de funções que poderiam ser incluídas em cada módulo:

#### matematica.py
```python
def media(lista):
    return sum(lista) / len(lista)

def mediana(lista):
    lista_ordenada = sorted(lista)
    n = len(lista_ordenada)
    meio = n // 2
    if n % 2 == 0:
        return (lista_ordenada[meio - 1] + lista_ordenada[meio]) / 2
    else:
        return lista_ordenada[meio]
```

#### texto.py
```python
def contar_palavras(texto):
    palavras = texto.split()
    return len(palavras)

def inverter_texto(texto):
    return texto[::-1]
```

#### data.py
```python
from datetime import datetime

def formatar_data(data, formato='%d/%m/%Y'):
    return data.strftime(formato)

def diferenca_entre_datas(data1, data2):
    return (data2 - data1).days
```

### Uso da Biblioteca
Para usar a biblioteca, você importaria o módulo necessário e chamaria as funções desejadas:

```python
from biblioteca_de_utilidades import matematica

lista_numeros = [23, 76, 58, 89, 34]
print("Média:", matematica.media(lista_numeros))
print("Mediana:", matematica.mediana(lista_numeros))
```

Esses são apenas exemplos iniciais. Você pode expandir cada módulo com mais funções conforme a necessidade. Lembre-se de escrever testes unitários para cada função para garantir que elas funcionem como esperado. Espero que isso ajude a começar o seu projeto de biblioteca de utilidades.
