# Item Components

All components used on items and weapons

## Durability
| Parameter | Type     | Range | Description                |
| :-------- | :------- | :---- | :------------------------- |
| `max_damage` | `int` | [0, 10000] | **Required**. The max amount of damage the item can take before being unusable |
| `damage_chance` | `float` | [0.0, 1.0] | **Required**. Used to determine the random chance that the item takes damage on use |
```json
"durability": {
    "max_damage": 0, 
    "damage_chance": 0.0
}
```

## Geometry
| Parameter | Type     | Range | Description                |
| :-------- | :------- | :---- | :------------------------- |
| `file_path` | `string` |  | **Required**. The path to the fbx file Ex. `geometries/items/item.fbx`  |
| `position` | `Vector3` |  | **Required**. The position the geometry is localized at |
| `rotation` | `Vector3` |  | **Required**. The rotation of the geometry |
| `scale` | `Vector3` |  | **Required**. The scale of the geometry |
| `pivot_point` | `Vector3` |  | **Required**. The pivot point that the rotation and position use to position the object |
```json
"geometry": {
    "file_path": "",
    "position": {
        "x": 0.0,
        "y": 0.0,
        "z": 0.0
    },
    "rotation": {
        "x": 0.0,
        "y": 0.0,
        "z": 0.0
    },
    "scale": {
        "x": 1.0,
        "y": 1.0,
        "z": 1.0
    },
    "pivot_point": {
        "x": 0.0,
        "y": 0.0,
        "z": 0.0
    }
}
```

## Material
| Parameter | Type     | Range | Description                |
| :-------- | :------- | :---- | :------------------------- |
| `material_type` | `int` | [0, 1] | **Required**. The type of material used on the geometry. (0 = Opaque, 1 = AlphaTest) |
| `color` | `Color` |  | **Required**. The main color that the material will use to apply to the texture |
| `main_tex_path` | `string` |  | **Required**. The path to the .png texture Ex. `textures/items/item.png` |
```json
"material": {
    "material_type": 0,
    "color": {
        "r": 1.0,
        "g": 1.0,
        "b": 1.0,
        "a": 1.0
    },
    "main_tex_path": "textures/items/rock.png"
},
```

## Stack Size
| Parameter | Type     | Range | Description                |
| :-------- | :------- | :---- | :------------------------- |
| `max` | `int` | [0, 10000] | **Required**. The max amount of the item that can be in a single stack |
```json
"stack_size": {
    "max": 64
}
```