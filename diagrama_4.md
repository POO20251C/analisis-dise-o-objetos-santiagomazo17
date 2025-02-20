diagrama.4
classDiagram
    class Album {
      +String titulo
      +String codigoID
      +String fechaLanzamiento
    }

    class Cliente {
      +String nombre
      +String idCliente
      +String fechaRegistro
    }

    class Compra {
      +String fechaCompra
      +bool devuelto
      +registrarDevolucion()
    }

    Album <|-- Compra : comprado
    Cliente <|-- Compra : realizado por
