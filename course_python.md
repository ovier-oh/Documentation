# Chapter 1

## Print 

Declaracion que al ejecutarse muestra ( o imprime) en pantalla el argumento que se introduce dentro de los parentesis. 

**Mostrar Texto**

Ingresamos entre comillas simples o dobles los caractecteres de texto que deben mostrarse en pantall. 

```
print("Hola mundo")
>> Hola mundo
```

**Mostrar Numeros**

Podemos entregarle a `print()` el numero que debe mostrar, o una operacion matematica a resovler. No empleamos comillas en estos casos. 

```
print(150 + 50)
>> 200
```

## String 

Los strings en Python son un tipo de dato formado por cadenas (o secuencias) de caracteres de cualquier tipo, formando un texto. 

**Concatenacion** 
    
Unificacion de cadenas de texto:
    
```
print("Hola" + " " + "mundo")
>> hola mundo
```

**Caracteres Especiales** 

Indicamos a la consola que el caracter a continuacion del simbolo `\` debe ser tratado como un caracter especial. 

```
\" > Imprime comillas 
\n > Separa texto en una nueva linea 
\t > Imprime un tabulador 
\\ > Imprime la barra invertida textualmente 

```

## Input 

Funcion que permite al usuario introducir informacion por medio del teclado el ejecutarse, otorgandole una instruccion acerca del ingreso solicitado. El codigo continuara ejecutandose luego de que el ususario realice la accion. 

```
input("Dime tu numbre: ")
>> Dime tu nombre: |
```
```
print("tu nombre es " + input("Dime tu nombre: "))
>> Dime tu nombre: Ovier 
>> Tu nombre es Ovier
```

## Tipos de datos 

En Python tenemos varios tipos o estructuras de datos, que son fundamentales en programacion ya que almacenan informacion, y nos permiten manipularla. 

```
texto (string)
>> "Python"
>> "750"
```

```
Numeros 
>> int 250 
>> float 12.50
```

```
booleanos
>> True 
>> False
```

| Estructuras        | Mutable  | Ordenado | duplicados |
|--------------------|----------|----------|------------|
| listas []          | check    | check    |check       |
| tuplas ()          | nope     | check    |check       |
| sets {}            | check    | nope     |nope        |
| diccionarios {}    | check    | nope*    |check/nope**|

*: En python 3.7+, existen consideraciones  
**: key es unica, value puede repertirse 


## Variables 

Las variables son espacios de memoria que almacenan valores o datos de distintos tipos, y (como su nombre indica) pueden variar. Se crean en el momento que se les asigna un valor, por lo cual en python no requerimos declararlas previamente. 

** Algunos ejemplos de uso 
```
pais = "Mexico"

nombre = input("Escribe tu nombre: ")
print("Tu nombre es " + nombre)

num1 = 55
num2 = 45
print(num1 + num2)
>> 100
```



### Nombres de las variables 

Existen convenciones y buenas practicas asociadas al nombre de las variables creadas en Python. Las mismas tienen la intencion de facilitar la interpretabilidad y mantenimiento del codigo creado. 

**Reglas** 

1. **Legible:**  nombre de la variable es relevante segun su contenido 
2. **Unidad:** no existen espacion (pueden incorporar guinoes bajos)
3. **Hispanismos:** Omitir signos especificos del idioma español, como tildes o la letra ñ.
4. **Numeros**: Los nombres de las variables no deben empezar por numeros (aunque puden contenerlos al final). 
5. **Signos/simbolos:** no se deben incluir: " ' , < > / ? | \ ( ) ! @ # $ % ^ & * ~ - + 
6. **Palabras Clave:**  no utilizamos palabras reservadas por Python. 


### Integers y Floats

Existen dos tipos de datos numericos basicos en Python: int y float. Como toda variable en Python, su tipo `type()` nos permite obtener el tipo de valor almacenado en una variable. 

**Int** 

`int` o integer, es unnumero entero, positivo o negativo, sin decimales, de un largo indeterminado. 

```
num1 = 7 
print(type(num1))
>> <class 'int'>
```

**Float**
Float, o "numero de punto flotante" es un numero que puede ser positivo o negativo, que a su vez contiene una o mas posiciones decimales. 

```
num2 = 3.141567 
print(type(num2))
>> <class 'float'>
```

### Conversiones 

Python realiza conversiones implicitas de tipos de datos automaticamente para operar con valores numericos. En otros casos, necesitaremos generar una conversacion de manera explicita. 

```
int(variable)
>> <class 'int'>

float(variable)
>> <class 'float'>
```

### Formatear cadenas 

Para facilitar la concatenacion de variables y texto en Python, contamos con dos herramientas que nos evitan manipular las variables, para incorporarlas directamente al texto:

- **Funcion format:** se encierra las posiciones de las variables entre corhcetes {}, y a continuacion del string llamamos a las variables con la funcion format. 

```
print("Mi auto es {} y de matricula {}".format(color_auto, maticula))
```

- **Cadenas literales (f-strigns):** a partir de Python3.8, podemos anticipar la concatenacion de variables antoponiendo _f_  al string 
  
```
print(f"Mi auto es {coloer_auto} y de matricula {matricula}")
```

### Operador Matematicos 

Veamos cuales son los operadores matemáticos basicos de Python, que utilizaremos para realizar calculos.

| Operador                      | Signo  | Ordenado                         |  
|-------------------------------|--------|----------------------------------|
| Suma                          | +      | check                            |
| Resta                         | -      | check                            |
| Multiplicación                | *      | nope                             |
| Division                      | /      | nope*                            |
| Cociente (division "al piso") | //     | nope*                            |
| Resto (modulo)                | %      | util para detectar valores pares |
| Potencia                      | **     | -                                |
| Raíz Cuadrada                 | **0.5  | es un caso especial              |

### Redondeo 

El redondeo facilita la interpretacion de los valores calculados al limitar la cantidad de decimales que se muestran en pantalla. Tambien, nos permite aproximar valores decimales el entero más próximo. 

```
round(valor a rendodear, cantidad de decimales[si se omite, es entero])
round(number, ndigits)
```

**Algunos ejemplos de uso**
```
print(round(100/3))
>> 33 

print(round(12/7, 2))
>> 1,71
```

### Index() 

Utilizamos el método `ìndex()` para explorar strign, ya que permite hallar el ñindice de aparicioón de un caracter o cadena de caracteres dento de un texto dado. 

```
string.index(value, start, end)
```

- `string` variable que almacena un string.
- `value` caracter(es) buscado(s).
- `start` Las aparaiciones antes del indice start se ignoran. 
- `end` Las apariciones luego del indice end se ignoran. 

```
string.rindex(value, start, end)
```
- `rindex()` busqueda en sentido inverso.

```
string[i]
```
- Devuelve el caracter en el indice i* 
  - En python, el indice en primera posición es el 0 
  
### Substrings 

Podemos extraer porciones de texto utilizando las herramientas de manipulacion de strings conocidad como slicing (rebanar). 

```
string[start:stop:step]
```

- `start`indice de inicio del sub-string (includo)
- `stop` indice del final del sub-string (no inluido)
- `step` paso

```
saludo = H O L A _ M U N D O 
         0 1 2 3 4 5 6 7 8 9 
print(saludo[2:6])
>> La_M

print(saludo[3::3])
>> aou 

print(saludo[::-1])
>> odnu;_aloH 
```

### Strings: Propiedades 

Esto es lo que debes tener presente al trabajar con strings en Python: 

- **Son inmutables:** una vez creados, no pueden modificarse sus partes, pero si pueden reasignarse los valores de las variables a través de métodos de strings. 
- **Concatenable:** es posible unir strings con el simbolo +.
- **Multiplicable:** es posible concatenar repeticiones de un string con el simbolo *.
- **Miltilinealess:** pueden escribirse en varias lineas al encerrarse entre triples comillas simples ('''') o dobles (""" """).
- **Determinar su longitud:** a través de la función `len(mi_string)`.
- **Verificar su contenido:** a través de las palabras clave `in` y `not in`. El resultado de esta verificación es un booleano (`True/False`).
  

### Strings: Métodos 

**Métodos de análisis**

`count():` retorna el número de veces que se repite un conjunto de
caracteres especificado.
```
"Hola mundo". count("Hola")
>> 1
```

`find()` e `index()`: retornan la ubicación (comenzando desde el cero) en la
que se encuentra el argumento indicado. Difieren en que index lanza
_ValueError_ cuando el argumento no es encontrado, mientras find retorna
_-1_.
```
"Hola mundo".find("world")
>> -1
```

`rfind()` y `rindex()`: Para buscar un conjunto de caracteres pero desde el
final.
```
"C:/python36/python.exe".rfind("/")
>> 11
```

`startswith()` y `endswith()` indican si la cadena en cuestión comienza o
termina con el conjunto de caracteres pasados como argumento, y
retornan True o False en función de ello.
```
"Hola mundo".startwith("Hola")
>> True
```

`isdigit()`: determina si todos los caracteres de la cadena son dígitos, o
pueden formar números, incluidos aquellos correspondientes a lenguas
orientales.
```
"abc123".isdigit()
>> False
```

`isnumeric()`: determina si todos los caracteres de la cadena son números,
incluye también caracteres de connotación numérica que no
necesariamente son dígitos (por ejemplo, una fracción).
```
"1234".isnumeric()
>> True
```

`isdecimal():` determina si todos los caracteres de la cadena son decimales;
esto es, formados por dígitos del 0 al 9.
```
"1234".isdecimal()
>> True
```

`isalnum():` determina si todos los caracteres de la cadena son
alfanuméricos.
```
"abc123".isalnum()
>> True
```

`isalpha():` determina si todos los caracteres de la cadena son alfabéticos.
```
"abc123".isalpha()
>> False
```

`islower():` determina si todos los caracteres de la cadena son minúsculas
```
"abcdef".islower()
>> True
```

`isupper():` determina si todos los caracteres de la cadena son mayúsculas
```
"ABCDE".isupper()
>> True
```

`isprintable():` determina si todos los caracteres de la cadena son
imprimibles (es decir, no son caracteres especiales indicados por \...)
```
"Hola \t mundo!".isprintalbe()
```

`isspace():` determina si todos los caracteres de la cadena son espacios.
```
"Hola mundo".isspace()
>> False
```

**Métodos de transformación**

En realidad los strings son inmutables; por ende, todos los métodos a
continuación no actúan sobre el objeto original sino que retornan uno nuevo.

`capitalize()` retorna la cadena con su primera letra en mayúscula.
```
"hola mundo".capitalize()
>> 'Hola mundo'
```

`encode():` codifica la cadena con el mapa de caracteres especificado y
retorna una instancia del tipo bytes
```
"Hola mundo".encode("utf-8")
>> b'Hola mundo'
```

`replace()` reemplaza una cadena por otra.
```
Hola mundo".replace("mundo", "world")
>> 'Hola world'
```

`lower():` retorna una copia de la cadena con todas sus letras en
minúsculas.
```
"Hola Mundo!".lower()
>> 'hola mundo!'
```

`upper():` retorna una copia de la cadena con todas sus letras en
mayúsculas.
```
"Hola Mundo!".upper()
>> 'HOLA MUNDO!'
```

`swapcase():` cambia las mayúsculas por minúsculas y viceversa.
```
"Hola Mundo!".swapcase()
>> 'hOLA mUNDO!
```

`strip()`, `lstrip()` y `rstrip()` remueven los espacios en blanco que preceden
y/o suceden a la cadena
```
" Hola mundo! ".strip()
>> 'Hola mundo!'
```

Los métodos `center()`, `ljust()` y `rjust()` alinean una cadena en el centro, la
izquierda o la derecha. Un segundo argumento indica con qué caracter se
deben llenar los espacios vacíos (por defecto un espacio en blanco).
```
"Hola".center(10, "*")
>> '***Hola***'
```

**Método de separación y unión**

`split()` divide una cadena según un caracter separador (por defecto son
espacios en blanco). Un segundo argumento en `split()` indica cuál es el
máximo de divisiones que puede tener lugar (-1 por defecto para
representar una cantidad ilimitada).

```
"Hola mundo!\nHello world!".split()
>> ['Hola', 'mundo!', 'Hello', 'world!'
```

`splitlines()` divide una cadena con cada aparición de un salto de línea
```
"Hola mundo!\nHello world!".splitlines()
>> ['Hola mundo!', 'Hello world!']
```
`partition()` retorna una tupla de tres elementos: el bloque de caracteres
anterior a la primera ocurrencia del separador, el separador mismo, y el
bloque posterior.
```
"Hola mundo. Hello world!".partition(" ")
>> ('Hola', ' ', 'mundo. Hello world!')
```
`rpartition()` opera del mismo modo que el anterior, pero partiendo de
derecha a izquierda.
```
"Hola mundo. Hello world!".rpartition(" ")
>> ('Hola mundo. Hello', ' ', 'world!')
```

`join()` debe ser llamado desde una cadena que actúa como separador
para unir dentro de una misma cadena resultante los elementos de una
lista.
```
", ".join(["C", "C++", "Python", "Java"])
>> 'C, C++, Python, Java'
```

### Listas 

Las listas son secuencias ordenadas de objetos. Estos objetos pueden ser datos de cualquier tipo: strings, integers, floats, booleanos, listas entre otros, Son tipos de datos mutables. 


- mutables 
- ordenado 
- admite duplicado 
  
```
lista_1 = ["C", "C++", "Python", "Java"]
lista_2 = ["PHP", "SQL", "Visual Basic"]
```

**Indexado: podemos acceder a los elementos de una lista a través de sus indices [inicio:fin:paso]

```
print(lista_1[1:3])
>> ["C++", "Python"]
```

**Cantidad de elementos:** a través de la propiedad `len()`
```
print(len(lista_1))
>> ["C++", "Python"]
```

