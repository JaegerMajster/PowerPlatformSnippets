// Przykładowe User Defined Types

// Tworzenie typu udtPerson z wykorzystaniem później zdefiniowanego typu udtAddress
udtPerson := Type (
    {
        FirsName: Text,
        LastName: Text,
        DateOfBirth: Date,
        Address: udtAddress
    }
);

// Tworzenie typu udtPeople będącego tablicą rekordów typu udtPerson
udtPeople := Type ([udtPerson]);

// Tworzenie typu udtAddress wykorzystanego powyżej do zdefiniowania typu udtPerson
udtAddress := Type (
    {
        AddressLine1: Text,
        AddressLine2: Text,
        City: Text,
        State: Text,
        Zip: Text
    }
)