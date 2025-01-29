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

Você pode usar _colchetes_ para fatiar as listas. A fatia `i:j` contém todos os elementos de i (incluído) a j(não incluído).
```python
   x = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

   x[:3] # [0, 1, 2]
   x[3:] # [3, 4, 5, 6, 7, 8, 9]
   x[-3:] #[7, 8, 9]
   x[1:5] #[1, 2, 3, 4]
   copy_of_x = x[:] # [0, 1, 2 ... 8, 9]
```

Para modificar a lista, você pode usar _extend_ e adicionar itens de outra coleção.
```python
   x = [1, 2, 3]
   x.extend([4, 5, 6]) # x = [1, 2, 3, 4, 5, 6]
```

```python
   x = [1, 2, 3]
   y = x + [4, 5, 6] # x = [1, 2, 3] e y = [1, 2, 3, 4, 5, 6]
```

###  6. 
```python
   
```