Las funciones son paquetes de códigos que los creamos para la reutilización de código sin repetir lineas, para crear una lo tenemos que hacer con la palabra reservada `func` luego viene el nombre de nuestra función y terminamos con `():`
```python
func jump():
	# Add upwards force
	# play animation
	# play sound

func _input(event):
	if event.is_action_pressed("my_action"):
		jump() # Run the function
```
>[!NOTE]
>Siempre que creamos un script ya viene con las funciones `_ready` y `_process` (En el caso de que seguiste la guía al pie de la letra entonces tambien viste la de `_input`)

Las funiones pueden tener entrada y salida de datos, a la entrada se le llama `parameters` y estos se encuentran dentro de los `()` de nuestra función. A la salida de datos se le llama `return` y esta se encuentra en el final de nuestra función
```python
func add(number1, number2): #ENTRADA DE DATOS
	var result = number1 + number2
	return result #SALIDA DE DATOS

print(add(5, 2)) #this is going to return 7
print(add(2, 2)) #this is going to return 4
var result_add = add(10, 20) #the result is going to be stored on the variable result_add (30)
result_add += add(1, 2) #is going to add the result of the function to the variable result_add(30) + function(3)
```
Otra cosa que podemos hacer es declarar el tipo de entrada de datos al igual que como hicimos cuando declaramos las variables, sumado a esto podemos definir el tipo de salida de dato con el `->` seguido del tipo de dato
```python
func add (number1: int, number2: int) -> int
# needs two int as parameters and returns an int
```
