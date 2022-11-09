# Mermaid 실습
- 순서도 실습
    - 첫번째 실습

```mermaid
classDiagram
    class Person{
        +name: str
        +phoneNumber: str
        +emailAddress: set
        +purchaseParkingPass()
    }

    class Address{
        <<abstract>>
        +street: str
        +city: str
        +state: str
        +postalCode: str
        +country: str
        -validata(): bool
        +outputAsLavel(): str
    }

    class Student{
        +studentNumber: int
        +studentMark: int
        +isElifibleToEnroll(str): bool
        +getSeminarsTaken(): int
    }

    class Professor{
        /salary: int
        #staffNumber: int
        -yearsOrService: int
        +numberOfClasses: int
    }

    Person <|-- Student
    Person <|-- Professor
    Person "0..1" --> "1" Address: lives at
    Professor "1..5" --> "0.." Student: supervises
```
