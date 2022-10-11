# Python para Cientistas de Dados - Parte 1
Anotações sobre essa seção do curso Geração Tech Unimed-BH - Ciência de Dados. Vai até os desafios iniciais.
## **Ambiente de  Desenvolvimento e Primeiros Passos com Python**
### História
- 1989 - inspirada em ABC
- 1991 - primeira versão pública (0,9)
- 2000 - list comprehensions
- 2001 - PSF (fundação)
- 2008 - Python 3 (não é retrocompatível)

Objetivos
- ser intuitivo
- ser um código aberto
- ser inteligível
- adequar-se a tarefas regulares com alta produtividade

Usos
- alta versatilidade
- NÂO é bom para mobile


## **Conhecendo a Linguagem de Programação Python**

## Tipos de dados
tipos informam as características dos valores para o interpretador: o que pode ser feito (operações), espaço exigido...

### Tipos padrão
- Texto
  - str (pode-se usar várias configurações de aspas)
- Numérico
  - int (inteiros), float (racionais), complex (complexos)
- Sequência
  - list, tuple, range
- Mapa
  - dict
- Coleções 
  - set, frozenset
- Booleano
  - bool (verdadeiro ou falso (0))
- Binário
  - bytes, bytearray, memoryview


## Modo interativo
permite ver o resultado na hora, sem ter que pedir para exibir informações
- **python**
- flag -i (python -i app.py)

## Constantes e variáveis

### Variáveis
- snake code: assim_com_underline
- nome sugestivo
- nome = "Julia"
- nome = "Julio
  
### Constantes
- LETRAS_MAIUSCULAS
- Python não tem palavra reservada p/ isso, é uma convenção
  
## Conversão de tipos
O Python reconhece automaticamente o tipo, porém é possível convertê-los
> numero_inteiro = 10  
> numero_float = 23,6  
- **float**(numero_inteiro) = 10.0  
- **int**(numero_float) = 23
- **str**(numero_inteiro) = 10
> texto = f"o número inteiro é {numero_inteiro}"
- print (texto)
  - o número inteiro é 10
  
## Funções de entrada e saída

### Entrada
- nome = **input**("Insira seu nome:")

### Saída
- **print**(nome)
- *end*="..."
- *sep*="_"

## **Tipos de Operadores com Python**

### Operadores artiméticos
- Soma: +
- Subtração: -
- Multiplicação: *
- Divisão: /
- Divisão inteira: // 
  - A divisão inteira só mostra os dígitos inteiros, sem arredondar
- Módulo: %
  - o que sobra de uma divisão
  - Ex: 10%3 retorna 1 (10/3 = 9, sobra 1)
- Exponenciação: **

Ordem matemática
- parênteses
- expoentes
- multiplicações e divisões, da esquerda p/ direita
- somas e subtrações, da esquerda p/ direita

### Operadores de comparação  
Usados para comparar dois valores 
- igualdade: ==
- diferença: !=
- maior que: >
- maior ou igual: >=
- menor que: <
- menor ou igual <=

### Operadores de atribuição
Definem o valor de uma variável
- simples: variável = valor
- adição: +=
- subtração: -=
- multiplicação, divisão, divisão inteira, múdulo e exponenciação seguem a mesma lógica
  
### Operadores lógicos
Retorna booleano (True ou False)  
OBS: 0 ou vazio é igual a False
- **and**
  - _todas_ as partes devem ser verdadeiras
- **or**
  - ao menos _uma_ das partes deve ser verdadeira
- **not**
  - inverte o valor de True para False e vice-versa

### Operadores de identidade
Compara de objetos ocupam a mesma posição na memória
> curso = "Curso de Python DIO" 
> nome_do_curso = curso  
> saldo, limite = 200, 200
- **is**: curso is nome_do_curso
  - True
- **is not**: curso is not nome_do_curso
  - False
- saldo is limite
  - True 

### Operadores de associação
Verifica se um objeto está em uma sequência
> curso = "Curso de Python"  
> frutas = ["maça", "melão", "morango"]  
> valor_saques  = [100, 200]
- **in**: "Python" in curso
  - True
- **not in**: "melancia" not in frutas
  - True
- in: 300 in saques
  - False
  

## **Estruturas condicionais e de repetição em Python**

### Indentação e blocos  
- Indentar auxilia na legibilidade do código, e o Python _exige_ isso
- 4 espaços em branco por nível de indentação 
- def módulo
  - o que faz parte do módulo deve ficar indentado:
  - coloca if
    - o que faz parte do if fica dentro

### Estruturas condicionais
Permitem o desvio do fluxo de controle: criam condições
- **if**
  - if condição:
    - fazer y
- **if/else**
  - bom para verdadeiro ou falso
  - if condição:
    - fazer y
  - else:
    - fazer z
- **if/elif/else**
  - para vários desvios. Digamos que há duas opções válidas:
  - if opção == 1:
    - fazer a
  - elif opção == 2:
    - fazer b
  - else:
    - mensagem de erro

- if aninhado
  - pode-se indentar ifs dentro de ifs

- if ternário
  - if em uma linha só
  > status = "Sucesso" if saldo >= saque else "Falha"  
  > print (f"{status} ao realizar o saque!")

### Estruturas de repetição
- **for**
  - quando sabemos o número de vezes que o código deve repetir, ou o objeto é iterável
  - bonus: else ao final do for
> texto = input("Insira um texto:")  
> VOGAIS - "AEIOU"
> 
> for letra in texto:  
> (indent) if letra.upper() in VOGAIS:  
> (indent2x) print (letra)

- **range(0, 4)**
> list(range(4))  
> [0,1,2,3]  
> for numero in range(0,51,5):  
> (indent)print(numero, end=" ")  
> 0, 5, 10, 15... 45, 50

- **while**
  - bom para chegarmos em um ponto específico, sem saber a quantidade de repetições
  - parece o if, mas repete
> opção = -1  
> while opção != 0:  
> (indent) opção = int(input"[1] Sacar \n[2] Extrato \n[0] Sair \n:"))  
> if opção == 1:  
> print("Sacando...")  
> elif opção ==2:   
> print("Exibindo o extrato...")
> else:
> print("Tenha um bom dia!")

- **break**
  - determina quando parar o programa em uma estrutura de repetição, em geral quando ela é infinita (while True)
- **continue**
  - pula a execução em alguma situação


## Manipulação de strings com Python

### Conhecendo métodos úteis da classe string
- **.upper**: coloca tudo em letra maiúscula
- **.lower**: coloca tudo em letra minúscula
- **.title**: primeiro caracter de cada palavra em letra maiúscula
- **.strip**: remove os espaços da esquerda e da direita
- **.lstrip**: remove os espaços do lado esquerdo (left)
- **.rstrip**: remove os espaços do lado direito (right)
- **.center(total de caracteres, caracter novo)**: centraliza palavra
  - ex: (curso.center(10, '#'))
  - "##Python##
- **"caracter a adicionar".join**(iterável)

### Interpolação de variáveis

- **%**: forma arcaica
  - %s, %d e %f no lugar da variável, para str, int e float, respectivamente
- **método format**: similar ao %
  - "{} nos lugares (com posição ou não) das variáveis" .format(variáveis)
  - entre {}, também pode-se colocar o nome da variável
  - outra opção: .format(***pessoa)
- **f strings**:
  - similar a format, sem o .format ao final
  - f"string com {variável}"
  - **espaços.quantidade de dígitos floatf**  
    - {PI:10.2f}

### Fatiamento de string
- **[start:stop:step]**
- utiliza-se o índice (0-based)
- nome[::-1]: espelha a string

### String múltiplas linhas
- **"""**: três aspas duplas no início e ao final
- mantém a formatação da string, com recuos e indentações