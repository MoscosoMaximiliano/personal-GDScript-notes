Los arrays son variables que contienen valores de cualquier tipo, como por dar un ejemplo, un `inventario` 
>[!NOTE]
>Si estas siguiendo la lista de temas, a partir de ahora toda declaración de variables se va a hacer con tipos, sino ir a la página [[Variables]]
```python
var inventory: Array[String] = ["Potion", "Sword", "Gold", 12]
```
En este ejemplo tenemos 3 items en nuestro inventario y para acceder a cada una de estas lo hacemos con el indice del mismo el cual siempre comienza desde cero
>[!NOTE]
>En la programación todo comienza desde el cero, ya que es lo que interpreta la computadora
```python
print(inventory[0]) # Print of the position 0 of the array = "Potion"
```
Tambien se pueden cambiar los valores de cada elemento del array
```python
inventory[1] = "Axe" # Change the value of the position 1 "Sword" for "Axe"
```

Algo a tener en cuenta de los Arrays, es que estos mismos tienen funciones a las que podemos acceder y nos van ayudar a facilitarnos el uso de las mismas
```python
inventory.remove_at(2) # Remove the value "Gold" from the array
inventory.append("Chestplate") # Add the value "Chestplate" to the array
```