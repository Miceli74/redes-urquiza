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
        +String name
        +List books
        +List members
        +List librarians
        +addMember(Member member)
    }

    Library "1" -- "contains" Book
    Library "1" -- "registers" Member
    Library "1" -- "manages" Librarian
