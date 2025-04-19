# Workflow pracy z promptami AI

Ten dokument opisuje standardowy proces tworzenia, aktualizacji i zarządzania promptami AI w projekcie.

## 1. Tworzenie nowego promptu

1. **Przygotowanie**:

- Zidentyfikuj konkretne zadanie, które ma wykonać AI
- Określ oczekiwane rezultaty
- Wybierz odpowiedni model AI z `metadata.md`

2. **Utworzenie struktury folderów**:

```bash
mkdir -p docs/prompts/[nazwa-funkcjonalności]/history
```

3. **Utworzenie pliku promptu**:

- Skopiuj szablon docs/templates/prompt-template.md do docs/prompts/[nazwa-funkcjonalności]/prompt.md
- Wypełnij wszystkie sekcje szablonu
- Dodaj odpowiednie tagi dla kategoryzacji

4. **Pierwsza wersja**:

- Skopiuj szablon docs/templates/version-prompt-template.md do docs/prompts/[nazwa-funkcjonalności]/history/v1.0.md
- Wypełnij metadane (data, model, rodzaj: "Start projektu")
- Skopiuj treść promptu z pliku prompt.md
- Wypełnij sekcję "Opis zmiany"

## 2. Aktualizacja istniejącego promptu

1. **Analiza potrzeb**:

- Zidentyfikuj problemy lub możliwości ulepszenia istniejącego promptu
- Określ konkretne zmiany do wprowadzenia

2. **Generowanie ulepszonej wersji**:

- Użyj reguł z prompt-rules.md do wygenerowania ulepszonej wersji
- Testuj na różnych modelach AI (minimum 2)

3. **Dokumentowanie nowej wersji**:

- Stwórz kolejny plik wersji, zwiększając numer wersji semantycznie:
  - Duże zmiany: v2.0, v3.0, itd.
  - Mniejsze usprawnienia: v1.1, v1.2, itd.
- Wypełnij wszystkie sekcje, w tym "Historia zmian" i "Rezultaty"

4. **Aktualizacja pliku głównego**:

- Zaktualizuj prompt.md najnowszą wersją promptu

## 3. Testowanie promptów

1. **Przygotuj przypadki testowe**:

- Zdefiniuj typowe scenariusze użycia
- Przygotuj przykładowe dane wejściowe

2. **Testuj na różnych modelach**:

- Użyj co najmniej 2 modeli z listy w metadata.md
- Dokumentuj różnice w wynikach

3. **Ocena wyników**:

- Wypełnij listę kontrolną jakości
- Zanotuj wszelkie nieoczekiwane zachowania

## 4. Najlepsze praktyki

- Prompty powinny być samowystarczalne
- Używaj jasnego, precyzyjnego języka
- Pamiętaj o odpowiednim kontekście
- Unikaj niejednoznaczności
- Regularnie przeglądaj i aktualizuj starsze prompty
- Dokumentuj zarówno udane, jak i nieudane próby

## 5. Zarządzanie metadanymi

1. **Aktualizacja tabeli modeli**:

- Gdy pojawiają się nowe modele, dodaj je do metadata.md
- Dokumentuj, do jakich zadań dany model sprawdza się najlepiej

2. **Linki w metadanych**:

- Upewnij się, że linki w pliku metadata.md wskazują na odpowiednie szablony

## 6. Współpraca między modelami AI

1. **Recenzja międzymodelowa**:

- Użyj jednego modelu do oceny i ulepszania promptów stworzonych przez inny model
- Porównuj różnice w interpretacji i generowanych odpowiedziach

2. **Iteracyjne doskonalenie**:

- Stosuj podejście iteracyjne, testując każdą wersję promptu na różnych modelach
- Dokumentuj specyficzne dla modelu reakcje na ten sam prompt

## 7. Wersjonowanie

1. **Konwencja nazewnictwa**:

- Pliki główne: prompt.md (zawsze aktualna wersja)
- Historia: v1.0.md, v1.1.md, v2.0.md itd.
