# Reto 2
## Receta de Cocina
Elija un problema de la vida real (sistema de gestión de biblioteca, negocio de compra-venta, automóvil, etc) que se pueda modelar a través de objetos y clases. Plantee las relaciones de clases, composiciones, propiedades y comportamientos del sistema en uno mas diagramas tipo UML.
***
```mermaid
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
***
```mermaid
classDiagram
    Ingredientes <|-- Alimento
    Ingredientes <|-- MaterialPreparación
    Ingredientes <|-- Utensilios
    Ingredientes : RecetaCocina
    class Alimento{
      +Tipo
      +GrupoAlimenticio
    }
    class MaterialPreparación{
      +Electrodomésticos
      +Recipientes
    }
    class Utensilios{
      +Platos
      +Cuchara
      +Tenedor
      +Cuchillo
    }
```
