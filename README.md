# Reto 2
## Receta de Cocina
```
classDiagram
    RecetaCocina "1" <|-- Ingredientes
    RecetaCocina "1" <|-- Pasos
    RecetaCocina "1" <|-- "1" Cocinero: Prepara
    Ingredientes <|-- Nombre
    Ingredientes <|-- Cantidad
    RecetaCocina : +Lista Ingredientes
    RecetaCocina : +Pasos
    class Ingredientes{
      +RecetaCocina
      +Nombre
      +Cantidad
    }
    class Pasos{
      +RecetaCocina
      +Número de paso
      +Descripción
    }
    class Cocinero{
    }
    class Nombre{
        +RecetaCocina
    }
    class Cantidad{
        +RecetaCocina
    }
```
