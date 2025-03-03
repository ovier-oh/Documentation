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
