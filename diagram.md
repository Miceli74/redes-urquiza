```mermaid
classDiagram
    class Libro {
        +String Titulo
        +String Autor
        +String isbn
        +boolean isAvailable()
    }

    class Miembro {
        +String Nombre
        +String ID
        +borrowBook(Book book)
        +returnBook(Book book)
    }

    class Bibliotecario {
        +String Nombre
        +String ID Empleado
        +addBook(Book book)
        +removeBook(Book book)
    }

    class Libreria {
        +String Nombre
        +List Libro
        +List Miembro
        +List Bibliotecario
        +addMember(Member member)
    }

    Library "1" -- "contains" Libro
    Library "1" -- "registers" Miembro
    Library "1" -- "manages" Bibliotecario
