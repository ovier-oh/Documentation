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

