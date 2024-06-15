Para modificar los nodos a través del código estos deben ser referenciados. Esto se puede lograr arrastrando el nodo sobre el editor de texto y queda algo como esto
```python
func _ready():
	#In this case we are using the node Label
	$Label.text = "Hello World"
	$Label.modulate = Color.GREEN
```