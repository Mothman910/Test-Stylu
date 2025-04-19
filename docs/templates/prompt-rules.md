# Reguły doskonalenia promptów, generowania nowych wersji

-Ulepsz następujący prompt [cel prompta], uwzględniając [nowe wymagania]:

[treść poprzedniego prompta]

-Stwórz dokumentację dla następującego promptu, uwzględniając jego historię wersji:

[treść promptu]
[lista zmian w wersjach]

-Po zakończeniu generowania, podpisz swoją odpowiedź aktualną nazwą modelu i datą.

## Formatowanie treści zewnętrznych

Przy włączaniu treści z zewnętrznych plików (np. project-vision.md) do promptów:

1. Zawsze poprzedzaj blok treści zewnętrznej jasnym nagłówkiem lub adnotacją wskazującą źródło, np. `### Wizja projektu (treść z project-vision.md)` lub `> (źródło: project-vision.md)`.
2. Możesz użyć:
   - zagnieżdżonego bloku kodu z innym typem oznaczenia niż główny blok (np. potrójne apostrofy `'''plaintext`)
   - **lub** bloku cytatu Markdown (`> ...`) – szczególnie gdy zależy Ci na czytelności i prostocie.
3. Nigdy nie używaj potrójnych backticks (```) do zagnieżdżonych bloków – zamiast tego użyj potrójnych apostrofów (`'''`) lub cytatu.
4. Przykład z blokiem cytatu:

   ```markdown
   ## Kontekst

   > (źródło: project-vision.md)
   >
   > # Wizja projektu "Test Stylu"
   >
   > ...
   ```

5. Przykład z blokiem kodu:

   ```markdown
   ## Kontekst

   ### Wizja projektu (treść z project-vision.md)

   '''plaintext

   # Wizja projektu "Test Stylu"

   ...
   '''
   ```
