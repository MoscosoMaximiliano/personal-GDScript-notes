Para que funcione los actions debemos crear los keybinds yendo a 
`Project > Project Settings > Input Map`
Estos keybinds se usan para crear todos inputs de nuestro juego. Para referenciar en el código nuestro nuevo keybind necesitamos crear la función de input
En este caso usamos un keybind llamado `my_action` que se ejecuta al tocar `spacebar`
```python
func _input(event):
	if event.is_action_pressed("my_action"):
		$Label.modulate = Color.RED
	if event.is_action_released("my_action"):
		$Label.modulate = Color.GREEN
```
