Son un tipo de dato parecido a los Arrays pero estos agregan mas información dando mas control sobre la información, esto se logra a través de la `key` y el `value`, vamos a dar un ejemplo.

Pensemos en un diccionario con definición de palabras y queremos buscar el significado de "caminar", en este caso, "caminar" es nuestra key, ya que su `value` va a ser la definición de la misma
```python
var word: String = "Caminar"
var dictionary = {
	"Caminar": "Andar determinada distancia."
} 
print(dictionary["Caminar"]) # Returns "Andar determinada distancia."
```
Se pueden agregar nuevos datos a los diccionarios diciendole la key y el value
```python
dictionary["Saltar"] = "Salvar de un salto un espacio o distancia."

print(dictionary["Saltar"])
```
Tambien podemos hacer uso de los loops para recorrer nuestros diccionarios y así ver el contenido de los mismos
```python
for key in dictionary:
	print(key + ": " + dictionary[key]) # here we concatenate strings with the + symbol
	# Output example: Caminar: Andar determinada distancia.
```
>[!NOTE]
>Al igual que los Arrays, los diccionarios pueden tener cualquier tipo de dato como value
```python
# Example of the note
var character = {
	 "name": "Hero", # String
	 "level": 12, # Int
	 "inventory": [ # Array
		 "Sword",
	 ], 
	 "stats": { # Dictionary
		"strenght": 3,
		# more info
	 } 
}
# for access to the array we need to call the key and the index
print(character["inventory"][0]) # Sword

# for access to the array we ned to call the key and the another key
print(character["stats"]["strenght"]) # 3
```
