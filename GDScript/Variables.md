Para crear una variable podemos hacerlo con la palabra clave `var`
```python
var health = 100

func _input(event):
	if event.is_action_pressed("my_action"):
		if health > 0:
			health -= 20
			print(health)
```
> [!NOTE]
>Para saber sobre lo que es la linea `if health > 0:` consultar en [If-statement](If-statement.md)
>Para saber sobre lo que es la linea `event.is_action_pressed("my_action"):` consultar en [Input](Input.md)

A continuación se va a mostrar una tabla de los tipos de asignación para la variable, todas estas son la versión resumida de hacer el algoritmo completo

| Simbolo | Definición  | ejemplo    |
| ------- | ----------- | ---------- |
| +=      | Sumar       | vida += 20 |
| -=      | Restar      | vida -= 20 |
| *=      | Multiplicar | vida *= 2  |
| /=      | Dividir     | vida /= 2  |

Tambien tenemos las variables constantes que se crean con la palabra clave `const` como por ejemplo el número pi, en el caso de las constantes, por recomendación de GODOT nos dice que siempre las escribamos en mayusculas (solo es una recomendación)
```python
const PI = 3.14
```

Algo a tener en cuenta sobre las variables es el `SCOPE` de la misma, es decir, el alcance que tiene la variable sobre nuest código

```python
var health = 100 # 0 tab level

func _ready():
	print(health) #
```
En este caso la variable health esta de manera global, es decir, la podemos usar en cualquier lugar ya que esta declarada sin estar en ninguna tabulación

```python
func _ready():
	var health = 100 # 1 tab levels
	if health == 100:
		var text = "Hello" # 2 tabs levels
		print(health) # This is going to works!!!
	print(text) # ERROR

func _process():
	print(health) # ERROR
```
Al contrario de este caso, la variable `health` solo se va a poder utilizar dentro de la función `_ready` y no dentro de la función `_process`, y sucede lo mismo con la variable `text`, esta solo funciona dentro del bloque de código del if

## Tipos de datos
Para las variables tenemos tipos de datos, si bien con la palabra clave `var` como vimos anteriormente podemos asignar cualquier tipo de dato, para nuestros juegos hay ocasiones que no podemos tomarnos este lujo y debemos ser mas precisos con los tipos de datos, a continuación vamos a ver los tipos de datos que podemos usar:

| Tipo    | Valor            |
| ------- | ---------------- |
| bool    | true / false     |
| int     | 231 / -231       |
| float   | 231,2 / -231,2   |
| string  | "Hello"          |
| Vector2 | Vector2(x, y)    |
| Vector3 | Vector3(x, y, z) |
>[!NOTE]
>En el caso de Vector2 y Vector3 estos tienen sus atributos que se pueden acceder de manera individual
>```python
># Example
>var position = Vector2(2, 3)
>position.x = 4
>position.y = 1
>```

Cuando convertimos un tipo de valor en otro, a esto se le llama `casting`
```python
var health_float = 100.0 # int

var health_text = str(health_float) # string -> "100.0"
var healt_int = int(health_float) # int -> 100
```

## Declarando Variables con Tipos
GDScript es de tipado dinamico, lo que quiere decir, es que este mismo puede crear una variable y asignarle cualquier tipo de dato sin problemas, pero tambien tiene el tipado estatico, el cual al crear la variable le decimos el tipo de dato de la misma y esta hace que no pueda cambiar a lo largo de la vida de la misma
```python
var health: int = 100
# Or
var health := 100 # is the same but more simple

func _ready():
	health = "string" # ERROR
```
Tambien podemos hacer que nuestra variable se exponga al editor de godot usando la palabra `@export`
```python
@export var damage := 100
```
![VariableExported](Images/VariableExported.png)

