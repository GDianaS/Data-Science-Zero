## Curso Intensivo de Python (Capítulo 2) ##

### 1. Módulos ###

```python
import [nome da biblioteca] as [apelido]
```

### 2. Funções ###

```python
def double (x): """
    Descrição da função. Por exemplo, esta função multiplica a entrada por 2. 
    """
    return x * 2
```

### 3. Strings (Cadeias de Caracteres) ###

As strings podem ser delimitadas por aspas simples ou duplas:
```python
    single_quoted_string = 'data science'
    double_quoted_string = "data science"
```
No Python, a barra invertida serve para codificar caracteres especiais. No entanto, é possível criar uma string _bruta_ com `r""`:
```python
    not_tab_string = r"\t" # representa os caracteres '\' e 't'
    len (not_tab_string) # é 2
```

#### União de Strings ####
```python
    first_name = "Joel"
    last_name = "Grus"

    full_name1 = first_name + " " + last_name
    full_name2 = "{0} {1}".format(fisrt_name, last_name)
    full_name3 = f"{first_name} {last_name}"
```
### 4. Exceções ###
```python
    try:
        print (0/0)
    except ZeroDivisionError:
        print("cannot divide by zero")
```
### 5. Listas ###
```python
    integer_list = [1, 2, 3]

    list_length = len(integer_list) # igual a 3
    list_sum = sum(integer_list) # igual a 6

    integer_list[0] # 1
    integer_list[1] # 2
    integer_list[2] # 3
```

Você pode usar _colchetes_ para fatiar as listas. A fatia `i:j` contém todos os elementos de i (incluído) a j(não incluído):
```python
   x = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

   x[:3] # [0, 1, 2]
   x[3:] # [3, 4, 5, 6, 7, 8, 9]
   x[-3:] #[7, 8, 9]
   x[1:5] #[1, 2, 3, 4]
   copy_of_x = x[:] # [0, 1, 2 ... 8, 9]
```

Para modificar a lista, você pode usar _extend_ e adicionar itens de outra coleção:
```python
   x = [1, 2, 3]
   x.extend([4, 5, 6]) # x = [1, 2, 3, 4, 5, 6]
```

```python
   x = [1, 2, 3]
   y = x + [4, 5, 6] # x = [1, 2, 3] e y = [1, 2, 3, 4, 5, 6]
```
Na maioria das vezes, acrescentaremos item por item ás listas:
```python
   x = [1, 2, 3]
   x.append(0) # x = [1, 2, 3, 0]
```

###  6. Tuplas 
São parecidas com as listas, no entanto, são imutáveis:
```python
   my_list = [1, 2]
   my_tuple = (1, 2)
```

As tuplas são uma forma eficaz de usar funções para retornar múltiplos valores:
```python
    def sum_and_product(x,y):
        return (x+y), (x*y)

    sp = sum_and_product(2, 3) # sp é (5, 6)
    s, p = sum_and_product(5, 10) # s é 5, p é 50
```

###  7. Dicionários
Associa valores a chaves e permite a rápida recuperação do valor correspondente a uma determinada chave:
```python
   empty_dict = {} # Dicionário vazio
   grades = {"Joel": 80, "Tim": 95} # 

   joels_grade = grades["Joel"] # igual a 80
```
Para verificar a existência de uma chave, você pode usar o `in`:
```python
   joel_has_grade = "Joel" in grades # Verdadeiro
   kate_has_grade = "Kate" in grades # Falso
```
O método `get` retorna um valor padrão (em vez de gerar uma exceção):
```python
   joels_grade = grades.get("Joel", 0) # igual a 80
   no_ones_grade = grades.get("No One") # o padrão é None
```
###  8. Conjuntos 
Coleção de elementos _distintos_
```python
   primes_below_10 = {2, 3, 5, 7}

   s = set() # conjunto vazio
   s.add(1) # {1}
   s.add(2) # {1,2}
   s.add(2) # {1,2}
   x = len(s) # 2
   y = 2 in s # Verdadeiro
```

###  9. Fluxo de Controle 
```python
    # if 
    if 1 > 2:
        message = "if only 1 were greater than two"
    elif 1 > 3:
        message = "else if"
    else:
        message = "when all else fails use else"
```

```python
    # ternário do tipo if-then-else
    parity = "even" if x % 2 == "odd"
```

```python
    # while
    x = 0
    while x < 10:
        print(f"{x} is less than 10")
        x += 1
```