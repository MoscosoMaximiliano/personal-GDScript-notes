Son condiciones que se tienen que cumplir para que se cumpla un bloque de código
La estructura de la misma se conforma de la palabra clave `if` seguido de la condición a verificar
Tambien esta la palabra clave reservada `else` que la utilizamos en el caso contrario de que nuestra condición no se pueda cumplir

A continuación tendrás una tabla con los condicionales que se pueden usar

| Condición | Significado   | Ejemplo    | Resultado |
| --------- | ------------- | ---------- | --------- |
| ==        | es igual a    | 1 == 1     | Verdadero |
| !=        | Distinto      | "a" != "b" | Verdadero |
| >         | Mayor a       | 3 > 2      | Verdadero |
| <         | Menor a       | 3 < 2      | Falso     |
| >=        | Mayor o igual | 3 >= 2     | Verdadero |
| <=        | Menor o igual | 3 <= 3     | Verdadero |
Algo que tambien podemos hacer es concatenar varias condiciones con las palabras reservadas `and` para referirnos a que se tienen que cumplir ambas y `or` para que se tiene que cumplir al menos una de ellas 
```python
var health = 50
var lives = 3
if health < 30 and lives == 0:
	print("WARNING")
else:
	print("You're okay")
	
# Another Example
var health = 50
var lives = 3
if health > 80 or lives >= 1:
	print("RUSH THE GAME")
else:
	print("Play safe my dude")
```
> [!NOTE]
> En caso de no saber lo que es `var` consultar en [[Variables]]

Tambien tenemos un caso mas que es el `elif`, este actua como combinación de ambos y se utiliza cuando queremos tener varias condiciones. Podemos poner cuantos `elif` querramos
```python
var health = 100
if health >= 80:
	print("You're healty")
elif health >= 50 and health < 80:
	print("You're okay")
elif health > 0 and health < 50:
	print("You're unhealthy!!!")
else:
	print("You diedaaaaaaaa")
```