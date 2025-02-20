diagrama.6
classDiagram
    class Galeria {
      +String nombre
      +List<Artista> artistas
      +List<Exposicion> exposiciones
      +agregarArtista(Artista)
      +agregarExposicion(Exposicion)
    }

    class Artista {
      +String id
      +String nombre
      +Date fechaRegistro
      +List<Obra> obras
      +presentarObras()
    }

    class Obra {
      +String titulo
      +String id
      +Date fechaCreacion
    }

    class Exposicion {
      +Date fechaInicio
      +Date fechaFin
      +bool estado
      +cambiarEstado(bool)
    }

    Galeria "1" o-- "*" Artista : registra
    Galeria "1" o-- "*" Exposicion : organiza
    Artista "1" o-- "*" Obra : crea
    Exposicion "1" o-- "1" Obra : exhibe
    Exposicion "1" o-- "1" Artista : presenta
