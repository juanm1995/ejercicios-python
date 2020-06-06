# Curso de Python

## ¿Qué es Python?

**Python** es un lenguaje de programación creado por **Guido Van Rossum**, con una sintaxis muy limpia, ideado para enseñar a la gente a programar bien. Se trata de un lenguaje interpretado o de script.

## Tabla de Contenido
- [Instalación](#instalación)
- [Antes de empezar](#antes-de-empezar)
- [Tipos de datos en Python](#tipos-de-datos-en-python)
- [Funciones](#funciones)
- [Variables](#variables)
- [Asignación de variables](#Asignación-de-variables)
- [Listas](#listas)
- [Tuplas](#tuplas)
- [Diccionarios](#diccionarios)
- [Conversiones](#conversiones)
- [Operadores Comunes](#operadores-comunes)
- [Métodos especiales](#métodos-especiales)
- [Condicionales IF](#condicionales-if)
- [Bucle FOR](#bucle-for)
- [Uso de Strings](#uso-de-strings)
  - [Comparación de strings y unicode](#comparación-de-strings-y-unicode)
  - [Cadenas](#Cadenas)
  - [Manejo de strings en Python](#manejo-de-strings-en-python)
  - [Separar cadenas de texto en Python](#separar-cadenas-de-texto-en-python)
- [Entradas](#Entradas)
- [Programas ramificados](#Programas-ramificados)
- [Iteraciones](#Iteraciones)
- [Bucles for](#Bucles-for)
- [Función range](#Función-range)
- [Programas numéricos](#Programas-numéricos)
  - [Representación de flotantes](#Representación-de-flotantes)
  - [Enumeración exhaustiva](#Enumeración-exhaustiva)
  - [Aproximación de soluciones](#Aproximación-de-soluciones)
  - [Búsqueda Binaria](#Búsqueda-Binaria)
  - [Factorial de un número con recursión](#factorial-de-un-número-con-recursión)
- [Funciones, alcance y abstracción](#Funciones,-alcance-y-abstracción)
- [Introducción al pensamiento computacional](#Introducción-al-pensamiento-computacional)
  - [Introducción al cómputo](#Introducción-al-cómputo)
  - [Lenguajes de programación](#Lenguajes-de-programación)

## Instalación

### Linux
Generalmente Linux ya lo trae instalado, para comprobarlo puedes ejecutar en la terminal el comando

**Versión 2.x**
```
python --version
```

**Versión 3.x**
```
python3 --version
```
Si el comando arroja un error quiere decir que no lo tienes instalado, en ese caso los pasos para instalarlo cambian un poco de acuerdo con la distribución de linux que estés usando. Generalmente el gestor de paquetes de la distribución de Linux tiene el paquete de Python

Si NO lo tienes instalado puedes usar este comando para instalar la versión 3.x en Ubuntu o Debian:
```
$ sudo apt-get install python3.x
```
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Antes de empezar

Para usar Python debemos tener un editor de texto abierto(yo utilizo Atom) y una terminal o cmd (línea de comandos) como administrador.

Para ejecutar Python abres la terminal y escribes:
```
$ python
```
Te abrirá una consola de Python, lo notarás porque el prompt cambia y ahora te muestra tres simbolos de mayor que “ >>> “ y el puntero adelante indicando que puedes empezar a ingresar comandos de python.
```
>>>
```
En éste modo puedes usar todos los comandos de Python o escribir código directamente.

*Si deseas ejecutar código de un archivo sólo debes guardarlo con extension.py y luego ejecutar en la terminal:
```
 $ python archivo.py
```
Ten en cuenta que para ejecutar el archivo con extensión “.py” debes estar ubicado en el directorio donde tienes guardado el archivo.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Tipos de datos en Python

**Enteros (int):** en este grupo están todos los números, enteros y long:
**ejemplo:** ```1, 2.3, 2121, 2192, -123```

**Booleanos (bool):** Son los valores falso o verdadero, compatibles con todas las operaciones booleanas ( and, not, or ):
**ejemplo:**: ```True, False```

**Cadenas (str):** Son una cadena de texto :
**ejemplo:** ```“Hola”, “¿Cómo estas?”```

**Listas:** Son un grupo o array de datos, puede contener cualquiera de los datos anteriores:
**ejemplo:** ```[1,2,3, ”hola” , [1,2,3] ], [1,“Hola”,True ]```

**Diccionarios:** Son un grupo de datos que se acceden a partir de una clave:
**ejemplo:** ```{“clave”:”valor”}, {“nombre”:”Fernando”}```

**Tuplas:** también son un grupo de datos igual que una lista con la diferencia que una tupla después de creada no se puede modificar:
**ejemplo:** ```(1,2,3, ”hola” , (1,2,3) ), (1,“Hola”,True) (Pero jamás podremos cambiar los elementos dentro de esa Tupla)```

**En Python trabajas con módulos y ficheros que usas para importar las librerías.**

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Funciones
Las funciones las defines con **def** junto a un nombre y unos paréntesis que reciben los parámetros a usar. Terminas con dos puntos.
```
def nombre_de_la_función(parametros):
```
Después por indentación colocas los datos que se ejecutarán desde la función:
```
 >>> def my_first_function():
 ...	return “Hello World!” 
 ...    
 >>> my_first_function()
Hello World!
```
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Variables
Las variables, a diferencia de los demás lenguajes de programación, no debes definirlas, ni tampoco su tipo de dato, ya que al momento de iterarlas se identificará su tipo. **Recuerda que en Python todo es un objeto.**
```
 A = 3 
 B = A
```
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Asignación de variables

Las **variables** son simplemente _nombres_ que se vinculan con un _valor en memoria_, y la forma en la que los _vinculamos_ es a través del **operador de asignación (=)**, y para _comparar_ su valor utilizamos **2 veces el operador de asignación (==).** La forma correcta de nombrar nuestras variables es darles un nombre _descriptivo_.

```py
# Tenemos unas variables que no entendemos que representan
a = 2
x = 4
z = (a * x) / 2

# Y las cambiamos por unas mas descriptivas
base = 2
altura = 4
area = (base * altura) / 2
```

También podemos **reasignar** valores a nuestras _variables_.

```bash
# A my_var le asignamos un valor
>>> my_var = 'Hello, world'
>>> print(my_var)
Hello, world

# Luego reasignamos otro valor
>>> my_var = 3
>>> print(my_var)
3
```

Cuando el espacio en memoria ya no tiene ninguna variable que la referencie, el **garabage collector** libera este espacio.

Cada uno de los lenguajes de programación tiene sus reglas. Algunas reglas para las variables en Python son:

- Pueden contener mayúsculas, minusculas, numeros(sin comenzar con uno) y el simbolo _
- No pueden llamarse como las **palabras reservadas**.

Los lenguajes tienen algo llamado **palabras reservadas**, estas son objetos dentro del lenguaje que ya tienen alguna función o valor asignado.

<br>
<div align="center"> 
  <img src="readme_img/reserved-words-python.png" width="500">
</div>
<br>

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Listas
Las listas las declaras con corchetes. Estas pueden tener una lista dentro o cualquier tipo de dato.
```
 >>> L = [22, True, ”una lista”, [1, 2]] 
 >>> L[0] 
 22
```
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Tuplas
Las tuplas se declaran con paréntesis, recuerda que no puedes editar los datos de una tupla después de que la has creado.
```
 >>> T = (22, True, "una tupla", (1, 2)) 
 >>> T[0] 
 22
```
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Diccionarios
En los diccionarios tienes un grupo de datos con un formato: la primera cadena o número será la clave para acceder al segundo dato, el segundo dato será el dato al cual accederás con la llave. Recuerda que los diccionarios son listas de **llave:valor**.
```
 >>> D = {"Kill Bill": "Tamarino", "Amelie": "Jean-Pierre Jeunet"} 
 >>> D["Kill Bill"]
 "Tamarino"
``` 
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Conversiones
De flotante a entero:
``` 
 >>> int(4.3)
 4
```  
De entero a flotante:
``` 
 >>> float(4) 
 4.0
``` 
De entero a string:
``` 
 >>> str(4.3) 
 "4.3"
``` 
De tupla a lista:
``` 
 >>> list((4, 5, 2)) 
 [4, 5, 2]
``` 
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Operadores Comunes
Longitud de una cadena, lista, tupla, etc.:
``` 
 >>> len("key") 
 3
``` 
Tipo de dato:
``` 
 >>> type(4) 
 < type int >
``` 
Aplicar una conversión a un conjunto como una lista:
``` 
 >>> map(str, [1, 2, 3, 4])
 ['1', '2', '3', '4']
``` 
Redondear un flotante con x número de decimales:
``` 
>>> round(6.3243, 1)
 6.3
``` 
Generar un rango en una lista (esto es mágico):
``` 
 >>> range(5) 
 [0, 1, 2, 3, 4]
``` 
Sumar un conjunto:
``` 
 >>> sum([1, 2, 4]) 
 7
``` 
Organizar un conjunto:
``` 
 >>> sorted([5, 2, 1]) 
 [1, 2, 5]
``` 
Conocer los comandos que le puedes aplicar a x tipo de datos:
``` 
 >>>Li = [5, 2, 1]
 >>>dir(Li)
 >>>['append', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
``` 
‘append’, ‘count’, ‘extend’, ‘index’, ‘insert’, ‘pop’, ‘remove’, ‘reverse’, ‘sort’ son posibles comandos que puedes aplicar a una lista.

Información sobre una función o librería:
``` 
 >>> help(sorted) 
 (Aparecerá la documentación de la función sorted)
``` 
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Clases
Clases es uno de los conceptos con más definiciones en la programación, pero en resumen sólo son la representación de un objeto. Para definir la clase usas class y el nombre. En caso de tener parámetros los pones entre paréntesis.

Para crear un constructor haces una función dentro de la clase con el nombre init y de parámetros self (significa su clase misma), nombre_r y edad_r:
``` 
 >>> class Estudiante(object): 
 ... 	def __init__(self,nombre_r,edad_r): 
 ... 		self.nombre = nombre_r 
 ... 		self.edad = edad_r 
 ...
 ... 	def hola(self): 
 ... 		return "Mi nombre es %s y tengo %i" % (self.nombre, self.edad) 
 ... 
 >>> e = Estudiante(“Arturo”, 21) 
 >>> print e.hola() 
 Mi nombre es Arturo y tengo 21
``` 
Lo que hicimos en las dos últimas líneas fue:

1. En la variable e llamamos la clase Estudiante y le pasamos la cadena “Arturo” y el entero 21.

2. Imprimimos la función hola() dentro de la variable e (a la que anteriormente habíamos pasado la clase).

Y por eso se imprime la cadena “Mi nombre es Arturo y tengo 21”

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Métodos especiales
**cmp**(self,otro)
Método llamado cuando utilizas los operadores de comparación para comprobar si tu objeto es menor, mayor o igual al objeto pasado como parámetro.

**len**(self)
Método llamado para comprobar la longitud del objeto. Lo usas, por ejemplo, cuando llamas la función len(obj) sobre nuestro código. Como es de suponer el método te debe devolver la longitud del objeto.

**init**(self,otro)
Es un constructor de nuestra clase, es decir, es un “método especial” que es llamas automáticamente cuando creas un objeto.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Condicionales IF
Los condicionales tienen la siguiente estructura. Ten en cuenta que lo que contiene los paréntesis es la comparación que debe cumplir para que los elementos se cumplan.
``` 
 if ( a > b ):
 	elementos 
 elif ( a == b ): 
 	elementos 
 else:
 	elementos
``` 
<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Bucle FOR
El bucle de for lo puedes usar de la siguiente forma: recorres una cadena o lista a la cual va a tomar el elemento en cuestión con la siguiente estructura:
``` 
 for i in ____:
 	elementos
``` 
Ejemplo:
``` 
 for i in range(10):
 	print i
``` 
En este caso recorrerá una lista de diez elementos, es decir el _print i _de ejecutar diez veces. Ahora i va a tomar cada valor de la lista, entonces este for imprimirá los números del 0 al 9 (recordar que en un range vas hasta el número puesto -1).

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Bucle WHILE
En este caso while tiene una condición que determina hasta cuándo se ejecutará. O sea que dejará de ejecutarse en el momento en que la condición deje de ser cierta. La estructura de un while es la siguiente:
``` 
 while (condición):
 	elementos
```   
Ejemplo:
``` 
 >>> x = 0 
 >>> while x < 10: 
 ... 	print x 
 ... 	x += 1
``` 
En este ejemplo preguntará si es menor que diez. Dado que es menor imprimirá x y luego sumará una unidad a x. Luego x es 1 y como sigue siendo menor a diez se seguirá ejecutando, y así sucesivamente hasta que x llegue a ser mayor o igual a 10.

**A continuación vamos a realizar ejercicios que te ayuden a comprender y poder aplicar cada una de las características de Python.**

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Uso de Strings
## Comparación de strings y unicode
Los strings tienen una característica muy importante: son inmutables, esto quiere decir que no se pueden cambiar después de que se han declarado.

Si quieres modificar el texto de un string debes definir un nuevo string y modificarlo usando funciones como slice.

**Comparación de strings**

Se pueden realizar operaciones con strings, por ejemplo comparar si son iguales o mayores o menores.

**Diferencia entre ASCII y Unicode**

Los caracteres también son números, para esto existen estándares que asignan un número a cada carácter, para generar un estándar se creó el ASCII pero esta solo toma en cuenta los caracteres en inglés, para dar soporte a más lenguajes se crea UNICODE.

Python codifica en ASCII por default, para cambiarlo por UNICODE debemos colocar u antes del string.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Cadenas

Las **cadenas** son secuencias de caracteres.

```py
'123'         #Esta es una cadena
```

Los _operadores_ que utilizamos tienen otros significados. Cuando utilizamos el operador **multiplicar (*)** lo que haremos es multiplicar la cadena por el numero de veces que deseamos, y con el operador **suma (+)** concatenaremos varias cadenas, sin embargo _Python_ nos permite concatenar de una forma mas legible.

```py
'123' * 3               # Con el operador *
'123123123'             # Obtenemos este resultado.

'123' + '456'           # Y el operador +
'123456'                # Concatenara las cadenas.

('Hip ' * 3) + 'hurra'  # Tambien podemos combinar operadores
'Hip Hip Hip hurra'

f'{"Hip " * 3}hurra'    # En Python podemos usar la expresion f para concatenar
'Hip Hip Hip hurra'
```

A las cadenas les podemos asignar diversas funciones:

- len: nos indica la longitud de la cadena.
- indexing: con esto podemos acceder a cada uno de los elementos de esta cadena a través de indices.
- slicing: podemos dividir las cadenas subcadenas.

```py
my_str = 'Hello, world!'    # Creamos una cadena

len(my_str)                 # Consultamos por su longitud
13

my_str[0]                   # Con slicing consultamos por el 1er caracter.
'H'

my_str[1]                   # Consultamos por el 2do caracter.
'e'

my_str[2]                   # Consultamos por el 3er caracter.
'l'

my_str[2:]                  # Traemos desde el 3er caracter hasta el final.
'llo, world!'

# Es importante indicar que los finales no son inclusivos.

my_str[:3]                  # Tremos desde el principio hasta el 3ro.
'Hel'

my_str[2:5]                 # Traemos desde el 3er caracter hasta el 5to.
'llo'

my_str[::2]                 # Traemos desde el principio hasta el final saltando de 2 en 2.
'Hlo ol!'
```

- Los objetos de tipo str pueden representarse con _comillas dobles (")_ o _comillas simples (')_
- El operador _suma (+)_ tiene diferente significado según el tipo de dato. Con **cadenas** significa _concatenación_.
- El operador _multiplicación (*)_ es el operador de _repetición_ con **cadenas**.
- Las cadenas son **inmutables**. Esto significa que una vez que creamos una cadena en memoria esta ya no puede cambiar, podemos reasignar la variable que la referencia a otro valor, pero la cadena en memoria no cambiara.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Manejo de strings en Python
Un string es una secuencia de caracteres, donde cada caracter tiene un indice que inicia en cero, por ejemplo
``` 
my_string = 'platzi'
``` 
``` 
my_string[0] # p
my_string[1] # l
my_string[2] # a
my_string[3] # t
my_string[4] # z
my_string[5] # i
``` 
Para conocer la longitud de un string podemos usar la funcion len

``` len(my_string) # 6``` 
Los string tienen algunos métodos útiles cómo:

``` my_string.upper() ``` # retorna el string en máyusculas
``` my_string.lower() ``` # retorna el string en minúscula
``` my_string.find('F') ``` # retorna el índice donde se encuentra

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Separar cadenas de texto en Python
La función slice de python nos permite separar los strings en substrings generando nuevas secuencias.

``` my_string = 'platzi'``` 

``` my_string[1:3] # la``` 

``` my_string[1:] # latzi``` 

``` my_string[1:6:2] # lti``` 

``` my_string[::-1] # iztalp``` 

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>


## Entradas

Las **entradas** son una forma recibir información para que las computadoras logren realizas cómputos.

- Python tiene la función input para recibir datos del usuario del programa
- Input siempre regresa cadenas, por lo que si queremos utilizar otro tipo, tenemos que hacer _type casting_. El _type casting_ es **transformar** el tipo de dato en otro, con esto podemos transformar el tipo y guardarlo en memoria asignandolo a una variable.

```bash
nombre = input('Cual es tu nombre: ')   # Utilizamos input para ingresar un nombre
Cual es tu nombre: Karl

print(nombre) # Vemos que contiene nuestra variable nombre
Karl

print(f'Tu nombre es {nombre}')   # Imprimimos una cadena concatenando una oracion con nuestra variable.
Tu nombre es Karl

numero = input('Escribe un numero: ')   # Utilizamos input para ingresar un numero
Escribe un numero: 45

numero    # Vemos que contiene nuestra variable numero
'45'

type(numero)    # Vemos el tipo de dato que es numero
<class 'str'>   # Y vemos que es un str

numero = int(input('Escribe un numero: '))  # Pero si definimos previamente el input como int
Escribe un numero: 45

type(numero)    # Nuestra variable numero sera de tipo int
<class 'int'>
```

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

# Programas ramificados

Para que nuestros programas realicen trabajos interesantes estos deben ser capaces de tomar decisiones, test o pruebas, es desde este concepto donde salen las **ramificaciones.** Dentro de los test que podemos realizar son los operadores de **comparación** y estos nos devolveras si la comparación es **verdadera (True)** o **falsa (False).**

- **Igual (==)**: Lo utilizaremos para comparar 2 objetos.
- **Distinto (!=)**: Verificamos que los objetos sean distintos.
- **Mayor que (>)**: Igual que en algebra, comparamos si el primer termino es mayor que el segundo.
- **Menor que (<)**: Verificamos que el primer termino sea menor que el segundo.
- **Mayor igual que (>=)**: Verificamos que el primer termino sea mayor igual al segundo.
- **Menor igual que (<=)**: Verificamos que el primer termino sea menor igual al segundo.

Ademas de los operadores de comparación también tenemos los operadores lógicos, estos son 3 **(and, or, not).**

<br>
<div align="center"> 
  <img src="readme_img/operador-logico.png" width="500">
</div>
<br>

Una vez que podemos entender bien los operadores de comparación y lógicos podemos generar nuestros **programas ramificados.** Una forma tipica de ocupar los operadores es con el método **if.**

```py
if condition:   # Evaluamos en primera instancia una condición.
    expresion
elif:           # En caso de que no se cumpla la condición anterior evaluamos nuevamente con otra.
    expresion
else:           # En caso de que no se cumpla ninguna condición.
    expresion

# En el ejemplo anterior pueden es obligatorio el 'if', sin embargo 'elif'
# y 'else' son opcionales. Pueden existir cuantos 'elif' queramos, pero solo
# puede haber 1 'if' y 1 'else'.

if 4 > 5:
    ...
elif 4 < 5:
    print('4 es menor que 5')
else:
    ...
```

Para poner en práctica esto crearemos un archivo _programas_ramificados.py_ y dentro de el escribiremos:

```py
num_1 = int(input('Escoge un entero: '))    # Preguntamos por un primer número.
num_2 = int(input('Escoge otro entero: '))  # Luego preguntamos por un segundo número.

if num_1 > num_2:       # Si el primer número es mayor que el segundo.
    print('El primer número es mayor que el segundo.')  # Imprimimos esta expresión.
elif num_1 < num_2:     # En caso de que el segundo sea mayor.
    print('El segundo número es mayor que el primero.') # Imprimiremos esta expresión.
else:   # En caso de que no cumpla ninguna condición.
    print('Los 2 números son iguales.')
```

Para ejecutar nuestro programa iremos a la terminal y escribiremos

```
python3 la/dirección/relativa/de/tu/archivo/programas_ramificados.py
```

y en consolo nos preguntara nuestros números y nos dara un resultado

```
Escoge un entero: 8
Escoge otro entero: 4
El primer número es mayor que el segundo.
```
```
Escoge un entero: 7
Escoge otro entero: 10
El segundo número es mayor que el primero.
```
```
Escoge un entero: 4
Escoge otro entero: 4
Los 2 números son iguales.
```

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Iteraciones

Las **iteraciones** nos permiten repetir las operaciones de una manera simple.

- La mayoría de las tareas computacionales no se pueden lograr con ramificaciones.
- Cuando queremos que un programa haga lo mismo varias veces, utilizaremos iteraciones.
- Se pueden escribir iteraciones dentro de iteraciones.
- Podemos utilizar _break_ para salir de una iteracion.
- Tener cuidado de iteraciones infinitas.

Para poner en práctica las iteracion crearemos el archivo _iteraciones.py_

```py
contador = 0

while contador < 10:
    print(contador)
    contador += 1   # contador = contador + 1
```

Luego iremos a la consola para ejecutar nuestro archivo.

```
python3 la/dirección/relativa/de/tu/archivo/iteraciones.py
```

y veremos que en nuestra consola se imprimiran los números del 0 al 9.

Si queremos que nuestro programa salga de la iteración cuando se cumpla cierta condición usaremos **break.**

```py
contador = 0

while contador < 10:
    print(contador)
    contador += 1       # contador = contador + 1

    if contador > 6:    # Cuando contador sea mayor que 6 terminara la iteracion.
        break
```

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Bucles for

Los bucles, en diversos lenguajes de programación pueden ser definidos o indefinidos. Los bucles definidos preestablecen las condiciones de la iteración por adelantado. Por su parte, los bucles indefinidos establecen la condición en la que una iteración terminará. En este último tipo de bucles existe el riesgo de que el bucle se vuelva infinito (cuando la condición de suspensión nunca se cumple).

Los bucles definidos se implementan en Python a través del keyword **for**. Por su parte, los bucles indefinidos se implementan con el keyword **while**.

Sin embargo, esta no es la única forma de implementar bucles definidos. Por ejemplo, Javascript puede implementar un bucle definido mediante el siguiente constructo:

```py
for (i = 0; i <= 10; i++) {
  <expresión>
}
```

El bucle se puede leer de la siguiente manera:

- Inicializa el bucle en 0
- Continua el bucle mientras **i** sea menor o igual que 10
- Incrementa i en uno al final de cada iteración

Es importante señalar que la expresión **i++** es equivalente a lo que en Python escribiríamos como **i += 1.**

Una segunda forma de crear un bucle definido es iterando en una colección de objetos. Esta es la forma que Python utiliza:

```py
for <variable> in <iterable>:
    <expresión>
```

### El bucle for en Python

En la definición anterior debemos entender <_iterable_> como una colección de objetos; y la <_variable_> como el elemento específico que se está exponiendo mediante el bucle en cada iteración.

```py
>>> frutas = ['manzana', 'pera', 'mango']
>>> for fruta in frutas:
        print(fruta)


manzana
pera
mango
```

### Iterables

En Python, un iterable es un objeto que se puede utilizar en un bucle definido. Si un objeto es iterable significa que se puede pasar como argumento a la función **iter**. El **iterable** que se pasa como parámetro a la función **iter** regresa un **iterator**.

```py
>>> iter('cadena')                  # cadena
>>> iter(['a', 'b', 'c'])           # lista
>>> iter(('a', 'b', 'c'))           # tupla
>>> iter({'a', 'b', 'c'})           # conjunto
>>> iter({'a': 1, 'b': 2, 'c': 3})  # diccionario
```

Todas las llamadas anteriores regresan un objeto de tipo **iterator**.

¿Qué pasa si le pasamos a la función **iter** un objeto que no en **iterable**? Obtendremos un **TypeError** que señala que el objeto no es un **iterable**. Esto es un ejemplo de programación defensiva en el que Python verifica el tipo del objeto antes de proceder al cómputo. ¡Intentalo en tu consola!

Es importante señalar que estos no son los únicos tipos de objetos que pueden ser **iterable**. Existen gran cantidad de ejemplos en la librería estándar y, de hecho, casi cualquier objeto se puede convertir en un **iterable** (pero eso ya lo veremos cuando hablemos de Python avanzado).

### Iterators

Ahora que ya sabemos cómo obtener un **iterator**, ¿Qué podemos hacer con él? Un **iterator** es un objeto que regresa sucesivamente los valores asociados con el iterable.

```py
>>> frutas = ['manzana', 'pera', 'mango']
>>> iterador = iter(frutas)
>>> next(iterador)
manzana
>>> next(iterador)
pera
>>> next(iterador)
mango
```

Como puedes ver, el **iterator** guarda el estado interno de la iteración, de tal manera que cada llamada sucesiva a **next** regresa el siguiente elemento. ¿Qué pasa una vez que ya no existan más elementos en el **iterable**? La llamada a **next** arrojará un error de tipo **StopIteration**.

### ¿Cómo implementa Python los bucles definidos?

Ahora ya conocemos todos los elementos necesarios para entender que es lo que sucede en Python cuando ejecutamos un bucle **for**. Considera nuevamente el siguiente código:

```py
>>> frutas = ['manzana', 'pera', 'mango']
>>> for fruta in frutas:
        print(fruta)
```

Este bucle se puede describir con los conceptos que explicamos previamente:

1. Python llama internamente la función **iter** para obtener un **iterator**
2. Una vez que tiene un **iterator** llama repetidamente la función next para tener acceso al siguiente elemento en el bucle.
3. Detiene el bucle una vez que se arroja el error **StopIteration**.

### Bucles for con diccionarios

Para iterar a lo largo de un diccionario tenemos varias opciones:

- Ejecutar el bucle **for** directamente en el diccionario, lo cual nos permite iterar a lo largo de las llaves del diccionario.
- Ejecutar el bucle **for** en la llamada **keys** del diccionario, lo cual nos permite iterar a lo largo de las llaves del diccionario.
- Ejecutar el bucle **for** en la llamada **values** del diccionario, lo cual nos permite iterar a lo largo de los valores del diccionario.
- Ejecutar el bucle **for** en la llamada **items** del diccionario, lo cual nos permite iterar en una tupla de las llaves y los valores del diccionario.

```py
estudiantes = {
    'mexico': 10,
    'colombia': 15,
    'puerto_rico': 4,
}

for pais in estudiantes:
    ...

for pais in estudiantes.keys():
    ...

for numero_de_estudiantes in estudiantes.values():
    ...

for pais, numero_de_estudiantes in estudiantes.items():
    ...
```

### Modificación del comportamiento de un bucle for

Podemos modificar el comportamiento de un bucle **for** mediante los _keywords_ **break** y **continue**.

**break** termina el bucle y permite continuar con el resto del flujo de nuestro programa.

**continue** termina la iteración en curso y continua con el siguiente ciclo de iteración.

### Conclusiones

Como pudimos observar, Python implementa los bucles definidos mediante los bucles **for**. Esta implementación nos permite iterar a lo largo de cualquier objeto que sea iterable. Para iterar necesitamos un iterador que nos regresará el siguiente valor en cada iteración. Todo esto, Python lo puede hacer por nosotros con el constructo **for ... in ...**.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

**Función range**

La función range nos permite generar un rango a partir de un número
```
range(5) # [0,1,2,3,4]
range(5, 40, 3)
```
**Iteraciones con for**

for nos permite recorrer un arreglo, asignando cada valor a una variable que decidas
```
for i in range(5):
    print(i)
```
Podemos operar los valores usando también condiciones, en este caso solo queremos elevar al cuadrado, los valores que sean divisibles por 3
```
for i in range(30):
  if i % 3 != 0:
    continue
  else:
    print(i**2)
```
La palabra reservada continue permite saltar a la siguiente iteración del ciclo y break permite salirse del ciclo.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

# Programas numéricos

## Representación de flotantes

La mayoría del tiempo los números flotantes (tipo **float**) son una muy buena aproximación de los números que queremos calcular con nuestras computadoras. Sin embargo, “la mayoría del tiempo” no significa todo el tiempo, y cuando no se comportan de esta manera puede tener consecuencias inesperadas.

Por ejemplo, trata de correr el siguiente código:

```py
x = 0.0
for i in range(10):
    x += 0.1

if x == 1.0:
    print(f'x = {x}')
else:
    print(f'x != {x}')
```

Es probable que te hayas sorprendido con el resultado. La mayoría de nosotros esperaríamos que imprimiera **1.0** en vez de **0.999999999999**. ¿Qué es lo que pasó?.

Para entender qué es lo que pasó tenemos que entender que es lo que pasa en la computadora cuando realizamos cómputos con números flotantes. Y para eso necesitamos entender números binarios.

Cuando aprendiste a contar, lo que en realidad aprendiste es una técnica combinatoria para manipular los siguientes símbolos que le llamamos números: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9.

La forma en la que funciona esta técnica es asignando el número 10 a la 0 al número de la extrema derecha, 10 a la 1 al siguiente, 10 a la 2 al siguiente y así sucesivamente. De tal manera que el número 525 es simplemente la representación de **(5 * 100) + (2 * 10) + (5 * 1)**.

Esto nos dice que el número de números que podemos representar depende de cuanto espacio tengamos. Si tenemos un espacio de 3, podemos representar 1,000 números (10 elevado a la 3) o la secuencia del 0 al 999. Si tenemos 4, podemos representar 10,000 (10 elevado a la 4) o la secuencia del 0 al 9,999. De manera general podemos decir que con una secuencia de tamaño n, podemos representar 10 elevado a la n números.

Los números binarios funcionan de la misma manera (de hecho cualquier número en cualquier base, por ejemplo, octales o hexadecimales). La única diferencia es cuántos símbolos tenemos para representar. En binario nada más tenemos 0, 1;
en hexadecimal tenemos 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, f.

De esta manera podemos decir que el número de la extrema derecha es **cantidad_de_simbolos^0**, **cantidad_de_simbolos^1**, **cantidad_de_simbolos^2**, etc. Por lo que en binario, que nada más tenemos 2 símbolos, decimos **2^0**, **2^1**, **2^2**, etc. Por ejemplo el número binario 101 es la representación de **(1 * 4) + (0 * 2) + (1 * 1)**, es decir 5.

Esta representación nos permite trabajar con todos los números positivos enteros dentro del computador, pero ¿Qué hacemos con los negativos y los racionales?.

El caso de los números negativos es sencillo: simplemente agregamos un bit adicional que representa el signo y la añadimos en la extrema izquierda. Por lo que el número **0**101 sería +5 y el número **1**101 sería -5.

El caso de los racionales es más complejo. En la mayoría de los lenguajes de programación modernos los racionales utilizan una implementación llamada punto flotante. ¿Cómo funciona esta representación?.

Antes de pasar a binario, vamos a pretender que estamos trabajando con una computadora basada en decimales. Un número flotante lo representaríamos con un par de enteros: los dígitos significativos y el exponente. Por ejemplo, el número 2.345 se representaría como **(2345 * 10^-3)** o **(2345, -3)**.

El número de dígitos significativos determinan la precisión con la que podemos representar número. Por ejemplo si nada más tuviéramos dos dígitos significativos el número 2.345 no se podría representar de manera exacta y tendríamos que convertirlo a una aproximación, en este caso 2.3.

Ahora pasemos a la verdadera representación interna de la computadora, que es en binario. ¿Cómo representarías el número 5/8 o 0.625? Lo primero que tenemos que saber es que 5/8 es en realidad el número **5 * 2^-3.** Por lo que podríamos decir (101, -11) (recuerda que el número 5 es 101 en binario y el 3 es 11).

Regresemos a nuestro problema inicial: ¿Cómo representaremos 1/10 (que escribimos en Python cómo 0.1)? Lo mejor que podemos hacer con cuatro dígitos significativos es (0011, -101) que es equivalente a 3/32 (0.09375). ¿Qué tal si tuviéramos cinco dígitos significativos? La mejor representación sería (11001, -1000) que es equivalente a 25/256 (0.09765625). ¿Cuántos dígitos significativos necesitamos entonces? Un número infinito. No existe ningún número que cumpla con la siguiente ecuación: **sim * 2^-exp**.

En la mayoría de las implementaciones de Python tenemos 53 bits de precisión para números flotantes. Así que los dígitos significativos para representar el número 0.1 es igual a:

11001100110011001100110011001100110011001100110011001 que es equivalente al número decimal: 0.1000000000000000055511151231257827021181583404541015625

Muy cercano a 1/10 pero no exactamente 1/10. Ahora ya sabemos la razón de esa respuesta tan extraña. Hay muy pocas situaciones en la que 1.0 es aceptable, pero 0.9999999999999999 no. Pero ¿Cuál es la moraleja de esta historia?

Hasta ahora hemos verificado igualdad con el operador **==**. Sin embargo, cuando estamos trabajando con flotantes es mejor asegurarnos que los números sean aproximados en vez de idénticos. Por ejemplo **x < 1.0 and x > 0.99999**.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Enumeración exhaustiva

También llamado "adivina y verifica" donde simplemente generamos todas las posibilidades. Técnicamente este no es un algoritmo eficiente, sin embargo, dependiendo del universo de posibilidades puede ser que sea el mas adecuado, ya que _las computadoras actuales son muy rapidas_ y por lo tanto la eficiencia de nuestro programa no es relevante, por lo tanto siempre ten en mente este tipo de **algoritmo** como uno de los **primeros en implementar**.

Vamos a crear un ejemplo de enumeración exhaustiva buscando la raíz cuadrada exacta de un numero.

```py
objetivo = int(input('Escoge un entero: '))

# Inicializamos respuesta como 0
respuesta = 0

# Mientras respuesta^2 sea menor que nuestro numero objetivo.
while respuesta**2 < objetivo:
    respuesta += 1  # Respuesta aumentara en 1.

if respuesta**2 == objetivo:
    print(f'La raiz cuadrada de {objetivo} es {respuesta}')

else:
    print(f'{objetivo} no tinene una raiz cuadrada exacta')
```

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Aproximación de soluciones

Es similar a la enumarción exhaustiva, pero no necesita una respuesta exacta, por lo tanto podemos aproximar soluciones con un margen de error que llamaremos **epsilon**.

Como siempre en programación debemos hacer un _trade-off_, no podemos ser precisos y rápidos a la ves, por lo tanto cuando nuestro **epsilon** es muy pequeño esto significa que debemos realizar **mas iteraciones** para llegar a la aproximación, lo cual significa sacrificar tiempo. Y por otro lado si queremos que nuestro **tiempo de ejecución** sea lo **mas corto posible** debemos sacrificar la **precisión** aumentando el valor de **epsilon**.

```py
objetivo = int(input('Escoge un numero: '))

epsilon = 0.01      # Definimos un margen de error.
paso = epsilon**2   # Los pasos para buscar la raiz sera igual a epsilon^2
respuesta = 0       # Inicializamos una respuesta 0


while abs(respuesta**2 - objetivo) >= epsilon and respuesta <= objetivo:
    respuesta += paso

if abs(respuesta**2 - objetivo) >= epsilon:
    print(f'No se encontró la raiz cuadrada de {objetivo}')
else:
    print(f'La raiz cuadrada de {objetivo} es {respuesta}')
```

Puedes intentar ir moviendo la magnitud de epsilon para obtener una mejor precisión o mejorar el tiempo de ejecución.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Búsqueda Binaria

Cuando la respuesta se encuentra en un conjunto ordenado, podemos utilizar **búsqueda binaria**. Es altamente eficiente, pues corta el espacio de búsqueda en dos por cada iteración. Los pasos que sigue son:

1. Consideramos como segmento inicial de búsqueda a la lista completa.
2. Analizamos el punto medio del segmento (el valor central), si es el valor buscado, devolvemos el índice del punto medio.
3. Si el valor central es mayor al buscado, podemos descartar el segmento que está desde el punto medio hacia la a derecha.
4. Si el valor central es menor al buscado, podemos descartar el segmento que está desde el punto medio hacia la izquierda.
5. Una vez descartado el segmento que no nos interesa, volvemos a analizar el segmento restante, de la misma forma.
6. Si en algún momento el segmento a analizar tiene longitud 0 o negativa significa que el valor buscado no se encuentra en la lista.

Para verlo de forma gráfica buscaremos el valor 18 en la lista [1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23].

<br>
<div align="center"> 
  <img src="readme_img/busqueda-binaria.png" width="500">
</div>
<br>

Para realizar un ejemplo práctico crearemos un programa para buscar raíces cuadradas.

```py
objetivo = int(input('Escoge un numero: '))

epsilon = 0.01  # Definimos nuestro margen de error.

bajo = 0.0      # Inicializamos la parte baja de nuestra busqueda como 0
alto = max(1.0, objetivo)   # Entre el numero que ingresamos y 1 vamos a tomar el mayor valor.
respuesta = (alto + bajo) / 2   # Definimos la mitad entre bajo y alto.

# Mientras el margen de error sea mayor a epsilon.
while abs(respuesta**2 - objetivo) >= epsilon:

    # Si ((alto+bajo)/2)^2 es menor a nuestro numero objetivo
    if respuesta**2 < objetivo:
        
        # Definimos la parte baja de nuestra busqueda como (alto + bajo)/2
        bajo = respuesta

    # En caso que (alto+bajo)/2 es mayor a nuestro numero objetivo
    else: 
        # Definimos la parte baja de nuestra busqueda como (alto + bajo)/2
        alto = respuesta

    # Luego definimos nuevamente la mitad entre alto y bajo.
    respuesta = (alto + bajo) / 2

# Cuando el ciclo ya alcance un error menor a epsilon imprimiremos el resultado.
print(f'La raiz cuadrada de {objetivo} es {respuesta}')
```

Este algoritmo es extremadamente rápido en comparación a los anteriores y esto es justamente lo que lo hace uno de los mas potentes.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Factorial de un número con recursión
En éste video hablaremos sobre la recursión, una función está siendo recursiva cuando dentro de el bloque de instrucciones que la conforma se usa a sí misma.

El concepto puede sonar complicado pero es muy común su uso, por ejemplo cuando haces el calculo del factorial de un número lo haces con una función recursiva:

**El factorial de un número es el número multiplicado por los números antes de el**, por ejemplo

```5! es 5*4*3*2*1```

Esto se puede expresar como
``` 
5*fac(4)
4*fac(3)
3*fac(2)
2*fac(1)
1*fac(0)
``` 
**Nota importante**: Cuándo estes trabajando con recursividad siempre debes pensar en el caso base, es decir debes definir el momento en el que la función dejará de llamarse a si misma, para que no hagas un loop infinito, por ejemplo en el caso del factorial terminas la ejecución cuando llegas a cero.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

# Funciones, alcance y abstracción

## Funciones y abstracción

La **abstracción** significa que no necesitas entender como funciona algo para utilizarlo. Un ejemplo de esto es una _calculadora_, en este caso no muchos saben como funciona el circuito interno de una calculadora, sin embargo esto no nos limita a utilizarlo, ya que solo necesitamos saber como operarlo.

Una de las habilidades mas importantes en la programación es la **abstracción**, ya que utilizaremos la mayoria del tiempo códigos y librerias de otras personas, por lo que solamente debemos saber operarlos.

La **decomposición** nos permite dividir el código en **componentes (funciones)** que colaboran con un fin en común. Esto se puede pensar como mini programas dentro de un programa mayor.

Para poder escribir una **función** en _Python_ lo hacemos con **def**

```py
# Las funciones se definen con 'def' luego del nombre y los parametros que necesitara.
def nombre(parametros):

    # Ejecutamos las expresiones que necesitemos
    cuerpo

    # Y retornaremos el valor que queramos. El return no es obligatorio.
    return expresion

# Aqui definimos una función suma
def suma(a, b):
    total = a + b
    return total

# Y para ejecutarlo simplemente llamamos a la
# función por su nombre e ingresamos los parámetros que necesita
suma(2, 3)
```
En las funciones existen los **valores por defecto**, esto significa que en caso de que no se ingrese el argumento este ya tendra un **valor por defecto.** Tambien existen los keywords que significa que al llamar la funcion podemos llamar al nombre del argumento para asignarles un valor.

```py
# Definimos una funcion con valor por defecto de "inverso = False"
def nombre_completo(nombre, apellido, inverso=False)
    if inverso:
        return f'{apellido} {nombre}'
    else:
        return f'{nombre} {apellido}'

# De forma ordena ingreso los valores a los parametros de la función.
# Sin embargo no es necesario ingresar un valor para "inverso" ya que
# tiene un valor por defecto ya asignado
nombre_completo('Karl', 'Behrens')

# En este caso ingresaremos el valor "True" para "inverso"
nombre_completo('Karl', 'Behrens', inverso=True)

# Con Keywords podemos ingresar las variables en el orden que
# deseamos mientras llamemos el valor del parametro y
# le asignamos el valor.
nombre_completo(apellido='Behrens', nombre='Karl')
```

**Recuerda:**

Para detener la ejecución de un ciclo, puede utilizar CTRL + C en la consola.

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

# Introducción al pensamiento computacional
## Introducción al cómputo

Posiblemente la primera computadora fue creada por los **antiguos griegos** el cual tenia el proposito de calcular las posiciones del Sol, Luna y algunos otros cuerpos celestes.

<br>
<div align="center"> 
  <img src="readme_img/computadora-griega.jpg" width="250">
  <h5>Mecanismo Anticitera</h5>
</div>
<br>

Miles de años despues se creo el **telar de Jacquard**, en donde las se creaban tarjetas con agujeros que representaban la información que tiene que hacer un pedazo de tela.

<br>
<div align="center"> 
  <img src="readme_img/Telar-de-Jacquard.jpg" width="350">
  <h5>Telar de Jacquard</h5>
</div>
<br>

Despues llego el **motor analítico de Charles Babbage**, el cual ocupo la tecnología de punta en su epoca para poder realizar cálculos.

<br>
<div align="center"> 
  <img src="readme_img/motor-babbage.jpg" width="350">
  <h5>Motor analítico de Charles Babbage</h5>
</div>
<br>

Durante el siglo IXX el gobierno de EE.UU. tenia serios problemas para realizar los censos como mandaba la constitución. En este momento fue cuando llego la **máquina tabuladora**, la cual se utilizo para realizar los censos con tarjetas, obteniendo resultados mas rápidos y certeros.

<br>
<div align="center"> 
  <img src="readme_img/maquina-tabuladora.jpg" width="350">
  <h5>Máquina Tabuladora</h5>
</div>
<br>

Antiguamente existia la **profesión de computadora**, la cual eran personas que se dedicaban a seguir ciertas instrucciones para obtener los resultados. Sin embargo estos resultados estaban plagados de errores. Al inicio del siglo XX ya existian compañias que tenian la necesidad de realizar calculos exactos y a gran escala. Es aquí donde llegan **Alan Turing** y **Alonzo Church** con la idea de que todos los algoritmos desarrollados por la humanidad podían ser reducidas a una maquina imaginaria, que tuviera una cinta infinita donde apuntarian símbolos y estos símbolos se pudieran manipular. Es aquí donde se comenzo la carrera para crear la primera computadora electrónica, el cual fue el **ENIAC**.

<br>
<div align="center"> 
  <img src="readme_img/church_alonzo.jpg" height="200">
  <img src="readme_img/alan-turing.jpg" height="200">
  <img src="readme_img/eniac.jpg" height="200">
  <h5>Alonzo Chruch, Alan Turing y la maquina ENIAC respectivamente.</h5>
</div>
<br>

**John von Neumann** se dio cuenta que en el hardware no solo se podía almacenar el poder de computo, tambien los programas para ejecutar. A esta arquitectura se le llama la **arquitectura de von Neumman.** De esta arquitectura nace la máquina **EDVAC** (Electronic Discrete Automatic Computer).

<br>
<div align="center"> 
  <img src="readme_img/neumann-edvac.jpeg" width="350">
  <h5>John von Neumann junto a la maquina EDVAC.</h5>
</div>
<br>

<br>
<div align="center"> 
  <img src="readme_img/arquitectura-neumann.png" width="350">
  <h5>La arquitectura von Neumann.</h5>
</div>
<br>

Con la llegada de los **microchips** llego la pauta para la computación de hoy en día. Estos microchips se hicieron tan pequeños con el tiempo usando la tecnología de la **fotónica.**

<br>
<div align="center"> 
  <img src="readme_img/microchips.jpg" height="200">
  <img src="readme_img/oblea-silicio.jpg" height="200">
  <h5>Microchip y Oblea de Silicio respectivamente.</h5>
</div>
<br>

Ya en nuestros tiempos llego la **nube**, el cual son data centers que no son mas que miles o millones de computadoras.

<br>
<div align="center"> 
  <img src="readme_img/nube.jpg" width="350">
  <h5>Sala de servidores de una nube</h5>
</div>
<br>

**Richar Feyman** nos dio las bases del computo cuantico, el pensaba que no podiamos simular los sistemas cuanticos si no teniamos una computadora cuántica, por lo cual hoy en día estamos en la carrera de la **computación cuantica.**

<br>
<div align="center"> 
  <img src="readme_img/feynman.jpeg" height="200">
  <img src="readme_img/computador-cuantico.png" height="200">
  <h5>Richard Feyman y una computadora cuántica respectivamente.</h5>
</div>
<br>

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>

## Lenguajes de programación

¿Cómo le damos instrucciones a las computadoras? Primero debemos saber que existen **conocimiento declarativo e imperativo.** El conocimiento **declarativo** define las relaciones que existen entre diversas variables, por ejemplo una fórmula matemática. En el caso del **imperativo** nos dice como llegar a un resultado, y dentro de este existen los **algoritmos.**

Un **algoritmo** es una _lista finita de instrucciones_ que describen un cómputo, que cuando se ejecuta con ciertas entradas _(inputs)_ ejecuta pasos intermedios para llegar a un resultado _(output)_. Los algoritmos se conocen desde los antiguos griegos, y fue la evolución de estos que nos dieron los primeros **lenguajes de programación.**

**Ada Lovelace** se dio cuenta que con las bases teóricas del _motor analítico_ podía calcular una serie de los _números de Bernoulli_, y así creo el primer programa de computación.

<br>
<div align="center"> 
  <img src="readme_img/lovelace.jpg" width="350">
  <h5>Ada Lovelace</h5>
</div>
<br>

**Grace Murray Hopper** fue pionera en el mundo de las ciencias de la computación y la primera programadora que utilizó el _Mark I_. Entre las décadas de los 50 y 60 desarrolló el primer compilador para un lenguaje de programación así como también propició métodos de validación. Grace se le ocurrió la idea de tomar unas instrucciones de 1 y 0 para simplificarlos en una instrucción mas entendible para las personas, idea que fue el punta pie inicial para los **lenguajes de programación modernos.**

<br>
<div align="center"> 
  <img src="readme_img/Grace-Murray-Hopper.jpg" width="350">
  <h5>Grace Murray Hopper</h5>
</div>
<br>

En el sentido de la idea de los lenguajes de programación llega **Dennis Ritchie**, el cual fue el inventor del lenguaje _C_, posiblemente uno de los lenguajes mas importantes de la historia.

<br>
<div align="center"> 
  <img src="readme_img/dennis-ritchie.jpg" width="350">
  <h5>Dennis Ritchie</h5>
</div>
<br>


**Guido van Rossum**, tenia en mente crear un lenguaje de programación que fuera lo mas comprensible posible, eliminando símbolos y sintaxis extrañas, cercano al lenguaje natural. Fue por esta idea en donde nació _Python_.

<br>
<div align="center"> 
  <img src="readme_img/van-rossum.jpg" width="350">
  <h5>Guido van Rossum</h5>
</div>
<br>

<div align="right">
  <small><a href="#tabla-de-contenido">volver al inicio</a></small>
</div>
