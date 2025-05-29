# MongoWebGallery

**MongoWebGallery** to aplikacja internetowa stworzona jako część pracy inżynierskiej. Jej celem jest umożliwienie użytkownikom dodawania, przeglądania i zatwierdzania wpisów opisujących różne technologie programistyczne. Projekt wykorzystuje bazę danych MongoDB oraz platformę ASP.NET Core MVC.

## 📌 Opis projektu

Aplikacja pełni rolę galerii technologii – użytkownicy mogą zgłaszać nowe technologie wraz z opisem i grafiką, a administrator ma możliwość ich zatwierdzania lub usuwania. Tylko zatwierdzone technologie są widoczne publicznie.

Projekt został zrealizowany zgodnie z dobrymi praktykami inżynierskimi, z uwzględnieniem autoryzacji, ról użytkowników oraz struktury zgodnej z zasadą separacji warstw (MVC).

## 🛠️ Technologie

- **ASP.NET Core MVC** – backend i logika aplikacji
- **MongoDB** – baza danych NoSQL do przechowywania wpisów o technologiach
- **Identity (ASP.NET Core Identity)** – zarządzanie użytkownikami i rolami (Admin / User)
- **Razor Views** – tworzenie interfejsu użytkownika
- **Bootstrap** – stylowanie frontendowe
- **C#** – język programowania

## ⚙️ Funkcjonalności

### Użytkownik (rola: `User`)
- Rejestracja i logowanie
- Dodawanie technologii (nazwa, opis, grafika)
- Przeglądanie zatwierdzonych technologii

### Administrator (rola: `Admin`)
- Panel zarządzania technologiami
- Zatwierdzanie lub usuwanie zgłoszonych technologii

## 🧑‍💻 Struktura projektu

- `Controllers/` – kontrolery odpowiedzialne za logikę aplikacji
- `Models/` – modele danych (np. `Technology.cs`)
- `Views/` – widoki Razor (.cshtml)
- `Program.cs` i `Startup.cs` – konfiguracja aplikacji i serwisów
- `wwwroot/` – pliki statyczne (grafiki, style)

## ▶️ Uruchomienie projektu

1. **Wymagania:**
   - .NET 7 SDK lub wyższy
   - MongoDB (lokalnie lub w chmurze, np. MongoDB Atlas)
   - Visual Studio 2022+ lub VS Code

2. **Konfiguracja połączenia z MongoDB:**

   W pliku `appsettings.json` dodaj:

   ```json
   "MongoDbSettings": {
     "ConnectionString": "mongodb://localhost:27017",
     "DatabaseName": "TechnologyGallery"
   }
