Los loops son sentencias que se van a repetir n cantidad de veces basado en una condición, esto se utiliza para facilitar el manejo del código del cual desconocemos sus dimensiones
```python
var inventory: Array[String] = ["Sword", "Chestplate", "Potion", "Gold"]
for item in inventory:
	print(item) # Going to show the items of the inventory

# An example more complex to how utils is the loops
# Let's gonna show the items who only has equals or more than 5 characters
for item in inventory:
	if item.length >= 5:# length returns the quantity of characters
		print(item)
```
Este fue un ejemplo con una variable de tipo array, pero tambien podemos definir un loop que se repita una cantidad de veces que nosotros determinemos
```python
for n in 10: # n always start on 0, and it's going to 7
	print(n) # returns the number of the iteration 0, 1, 2, 3, 4, 5, 6, 7
```
Tenemos otro tipo de loop el cual es el `while`, este se diferencia del `for` porque se ejecuta indefinidamente basado en una condición, siempre que la condición sea verdadera se va a ejecutar
```python
var health: Int = 100

func generate_monsters():
	# Spawn monsters logic

while(health > 0):
	# Code logic
	generate_monsters() # Is going to call the functions always the health is greater than 0
	# More code logic

print("Player Died") # Is printed when the condition of the while is false
```
Tambien tenemos dos palabras claves que se pueden utilizar en el `while` que son `break` el cual se utiliza para terminar el ciclo while y el `continue` que va a seguir con su trayecto, supongamos que en la entrada del ciclo del while, golpean a nuestro personaje y se queda con 0 de vida, nosotros en vez de recorrer todo el while, podemos validar el estado de la vida y así evitar tener que recorrer todo el ciclo
```python
var health: Int = 100

func generate_monsters():
	# Spawn monsters logic

while(health > 0):
	if health <= 0:
		break # Stop the while cycle
	# Code logic
	generate_monsters() # Is going to call the functions always the health is greater than 0
	# More code logic

print("Player Died") # Is printed when the condition of the while is false
```
>[!NOTE]
> Hay que tener mucho cuidado con el `while` porque puede generar un loop infinito ya que la condición siempre se cumple, por ejemplo poner `while(true):`