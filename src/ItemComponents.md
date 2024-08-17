# Item Components

All components used on items and weapons

## Durability
| Parameter | Type     | Range | Description                |
| :-------- | :------- | :---- | :------------------------- |
| `max_damage` | `int` | [0, 10000] | **Required**. The max amount of damage the item can take before being unusable |
| `damage_chance` | `float` | [0.0, 1.0] | **Required**. Used to determine the random chance that the item takes damage on use |
```json
"durability": {
    "max_damage": 0, // The max damage before the tool breaks / stops working
    "damage_chance": 0.0 // The chance multiplier of the tool taking damage
}
```

## Stack Size
| Parameter | Type     | Range | Description                |
| :-------- | :------- | :---- | :------------------------- |
| `max` | `int` | [0, 10000] | **Required**. The max amount of the item that can be in a single stack |
```json
"stack_size": {
    "max": 64 // The max amount of items that can fit in a stack | Note: Value must be between 1 and 10,000
},
```