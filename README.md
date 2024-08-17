# Jadens Multiplayer Shooter Modding Docs

## Items
### Structure

This is the key to creating custom items. All item properties define the characteristics of an Item.
| Parameter | Type     | Range | Description                |
| :-------- | :------- | :---- | :------------------------- |
| `identifier` | `object` |  | **Required**. Used for setting the name, id, description ect. |
| `components` | `object` |  | **Optional**. Used to add custom features to the Item |
```
{
    "identifier": {},
    "components": {}
}
```
### Identifier
The identifier property contains key information for displaying the Item. This property is the only required property.
| Parameter | Type     | Range | Description                |
| :-------- | :------- | :---- | :------------------------- |
| `name` | `string` |  | **Required**. The name displayed for the Item |
| `id` | `string` |  | **Required**. the items unique ID, must be all lowercase |
| `description` | `string` |  | **Required**. The description of the Item |
```
{
    "identifier": {
        "name": "",
        "id": "",
        "description": ""
    }
}
```
### Components
The components property contains all custom properties for an Item. These are completely optional but some are recommended to use such as stack size shown below.
```
{
    "identifier": {
        "name": "",
        "id": "",
        "description": ""
    },
    "components": {
        "stack_size": {
            "max": 64
        }
    }
}
```
See all [Item Components](https://github.com/Jaden-Allen/multiplayer_shooter/blob/main/src/ItemComponents.md)

