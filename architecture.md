<!-- Wygenerowano przez prompt: docs/prompts/project-init/prompt.md -->

# Architektura aplikacji "Test Stylu"

## 1. Diagram Architektoniczny (Opis Tekstowy)

Aplikacja będzie miała prostą architekturę po stronie klienta, typową dla aplikacji mobilnych React Native działających offline:

- **Warstwa Prezentacji (UI Layer):** Komponenty React Native odpowiedzialne za wyświetlanie interfejsu użytkownika (ekrany quizu, wyników, nawigacja) i obsługę interakcji użytkownika.
- **Warstwa Logiki Biznesowej (Logic Layer):** Moduły JavaScript zarządzające stanem aplikacji (np. aktualne pytanie, odpowiedzi użytkownika, wynik), logiką przepływu quizu i obliczaniem wyników.
- **Warstwa Danych (Data Layer):** Odpowiedzialna za dostarczanie danych do aplikacji. W tym przypadku będą to dane quizu (pytania, opcje odpowiedzi w formie obrazów, referencje naukowe) przechowywane lokalnie w aplikacji (np. w plikach JSON lub zaszyte w kodzie).

## 2. Główne Komponenty i Odpowiedzialności

- **`AppNavigator`:** Zarządzanie nawigacją pomiędzy ekranami aplikacji (np. ekran startowy, ekran quizu, ekran wyników).
- **`QuizScreen`:** Główny ekran quizu. Wyświetla aktualne pytanie, opcje odpowiedzi (obrazy), obsługuje wybór użytkownika i przechodzi do następnego pytania.
- **`ResultScreen`:** Wyświetla wynik quizu po jego zakończeniu, wraz z ewentualnymi wyjaśnieniami lub referencjami.
- **`QuizEngine` (Serwis/Logika):** Moduł zawierający logikę quizu: ładowanie pytań, śledzenie postępu, obliczanie wyniku na podstawie odpowiedzi.
- **`DataService` (Serwis):** Odpowiedzialny za ładowanie i dostarczanie danych quizu (pytań, obrazów, tekstów) z lokalnego źródła.
- **Komponenty UI (`components/`):** Mniejsze, reużywalne komponenty interfejsu (np. przyciski, karty z obrazami, wskaźniki postępu).

## 3. Uzasadnienie Wyboru Technologii

- **Frontend:** React Native - Zgodnie z wymaganiem w `project-vision.md`. Pozwala na tworzenie aplikacji na platformę Android (i potencjalnie iOS w przyszłości) przy użyciu jednej bazy kodu (JavaScript/TypeScript).
- **Zarządzanie Stanem:** React Context API (dla prostych potrzeb) lub biblioteka typu Zustand/Redux Toolkit (dla bardziej złożonego stanu w przyszłości). Wybór zależy od skomplikowania przepływu danych.
- **Nawigacja:** React Navigation - Popularna i dobrze wspierana biblioteka do nawigacji w aplikacjach React Native.
- **Animacje:** React Native Animated API lub biblioteka Reanimated - Do implementacji płynnych przejść i efektów wizualnych, zgodnie z wymaganiem.
- **Przechowywanie Danych:** Dane quizu (pytania, obrazy) będą częścią pakietu aplikacji (np. w folderze `src/data` lub `src/assets`). Obrazy zostaną zaimportowane bezpośrednio.
- **Backend/Baza Danych:** Zgodnie z wizją projektu, aplikacja działa w trybie offline, więc nie jest wymagany dedykowany backend ani zewnętrzna baza danych.

## 4. Struktura Folderów i Plików (Proponowana)

```
/Test Stylu
├── android/              # Natywny kod Android
├── ios/                  # Natywny kod iOS
├── src/
│   ├── assets/           # Zasoby statyczne
│   │   ├── images/       # Obrazy używane w quizie i UI
│   │   └── fonts/        # Czcionki (jeśli niestandardowe)
│   ├── components/       # Reużywalne komponenty UI
│   ├── screens/          # Komponenty reprezentujące ekrany aplikacji
│   │   ├── QuizScreen.js
│   │   └── ResultScreen.js
│   ├── navigation/       # Konfiguracja i logika nawigacji
│   │   └── AppNavigator.js
│   ├── services/         # Logika biznesowa, dostęp do danych
│   │   ├── QuizEngine.js
│   │   └── DataService.js
│   ├── store/            # Zarządzanie stanem (opcjonalnie, np. Zustand/Redux)
│   ├── styles/           # Style globalne, motywy
│   └── data/             # Dane quizu (np. questions.json)
├── .gitignore            # Pliki ignorowane przez Git
├── package.json          # Zależności i skrypty projektu
├── README.md             # Opis projektu
├── architecture.md       # Ten plik
└── docs/                 # Dokumentacja (istniejący folder)
    └── ...
```

## 5. Zawartość Podstawowych Plików Konfiguracyjnych

_Zawartość zostanie dodana w kolejnych krokach (patrz poniżej)._

## 6. Plan Kolejnych Kroków Rozwoju

1.  **Inicjalizacja projektu React Native:** Użycie `npx react-native init .`.
2.  **Utworzenie struktury folderów:** Stworzenie katalogów wewnątrz `src/` zgodnie z proponowaną strukturą.
3.  **Implementacja Nawigacji:** Skonfigurowanie podstawowej nawigacji między ekranami przy użyciu React Navigation.
4.  **Stworzenie Ekranów:** Zaimplementowanie szkieletów `QuizScreen` i `ResultScreen`.
5.  **Podgląd:** Umożliwienie podglądu działania aplikacji w przeglądarce na komputerze za pomocą przeglądarki Opera lub emulatora BlueStack w Windows 11.
6.  **Implementacja Logiki Quizu:** Stworzenie `QuizEngine` i `DataService` do zarządzania przepływem quizu i ładowania danych.
7.  **Dodanie Danych:** Przygotowanie i dodanie przykładowych pytań, odpowiedzi (obrazów) i referencji.
8.  **Styling i Animacje:** Dopracowanie wyglądu aplikacji, dodanie stylów i animacji.
9.  **Testowanie:** Przeprowadzenie testów funkcjonalnych.
