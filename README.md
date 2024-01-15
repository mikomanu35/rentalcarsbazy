Projekt na przedmiot bazy danych w aplikacjach internetowych
1. Wprowadzenie:
Projekt "Online Car Rental" to kompleksowe rozwiązanie, pozwalające na zarządzanie flotą samochodów online. Obejmuje autoryzację użytkowników, zarządzanie rolami, przeglądanie, dodawanie, edycję i usuwanie samochodów oraz proces wypożyczania.

2. Struktura Rozwiązania:
Modele:
auta.cs (Model Auta):
Definiuje atrybuty samochodu, takie jak model, marka, kolor, rok produkcji, cena, dostępność.
Order.cs (Model Zamówienia):
Zawiera informacje o zamówieniu, w tym klucze obce do użytkownika i samochodu. Może być rozbudowywane o dodatkowe atrybuty zamówienia.
Konteksty Danych:
AutaDbContext.cs:

Komunikuje się z bazą danych SQL Server, zawiera DbSet dla samochodów, użytkowników i zamówień. Może być rozbudowywany o konfiguracje relacji i właściwości modeli.
RegisterDbContext.cs:

Rozszerza funkcjonalność ASP.NET Identity, konfigurując niestandardowe właściwości użytkownika, takie jak imię i nazwisko.
Kontrolery:
AutaController.cs:

Zarządza operacjami związanymi z samochodami, takimi jak przeglądanie, dodawanie, edytowanie, usuwanie.
HomeController.cs:

Odpowiada za strony główne i obsługę błędów.
RolesController.cs:

Kontroluje operacje związane z zarządzaniem rolami użytkowników, umożliwiając administratorom dynamiczną zmianę uprawnień.
UserController.cs:

Zarządza funkcjonalnościami związanymi z użytkownikami, takimi jak przeglądanie samochodów i wypożyczanie.
Serwisy Autoryzacji:
RolesController.cs:

Zapewnia funkcje do zmiany ról użytkowników, co wpływa na ich dostęp do różnych funkcji.
UserController.cs:

Obsługuje proces wypożyczania samochodu przez użytkownika.
3. Funkcjonalności:
Autoryzacja i Role:
Użytkownicy posiadają różne role, takie jak "Admin" i "User", co wpływa na ich dostęp do różnych funkcji w systemie.
Zarządzanie Samochodami:
Administratorzy mogą dodawać, edytować, usuwać i przeglądać informacje o samochodach, co odbywa się za pośrednictwem AutaController.
Wypożyczanie Samochodów:
Użytkownicy z rolą "User" mogą przeglądać dostępne samochody i składać zamówienia na wypożyczenie za pośrednictwem UserController.
Zmiana Roli Użytkownika:
Administratorzy mają możliwość dynamicznej zmiany ról użytkowników, co wpływa na ich dostęp do różnych funkcji w systemie.
4. Użyte Technologie:
ASP.NET Core:

Framework do budowy nowoczesnych aplikacji internetowych.
Entity Framework Core:

ORM umożliwiający efektywne korzystanie z bazy danych SQL Server.
Identity Framework:

Zapewnia funkcjonalności zarządzania tożsamością i autoryzacją użytkowników.
SQL Server:

Baza danych służąca do przechowywania informacji o samochodach, użytkownikach i zamówieniach.
5. Podsumowanie:
Projekt "Online Car Rental" to zaawansowany system, który integruje różne technologie, aby dostarczyć kompleksowe rozwiązanie do zarządzania wypożyczalnią samochodów online. Obejmuje autoryzację, zarządzanie rolami, obsługę samochodów i zamówień. Struktura projektu pozwala na elastyczne rozwijanie i dostosowywanie do zmieniających się potrzeb biznesowych.
