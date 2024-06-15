Para generar números aleatorios tenemos varias funciones de las cuales podemos usar para casos determinados

| Función     | Limite     |
| ----------- | ---------- |
| randf       | [0, 1]     |
| randi_range | [min, max] |
```python
var loot_poll = randf()
if loot_pool <= 0.2:
	print("You found a RARE item")

var quantity_monsters = randi_range(30, 120)
if quantity_monsters > 90:
	print("Too many monsters")
elif quantity_monsters >= 30 and quantity_monsters <= 70:
	print("You're lucky")
```