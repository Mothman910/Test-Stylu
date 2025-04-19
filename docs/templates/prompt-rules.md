# Reguły doskonalenia promptów, generowania nowych wersji

-Śledź zmiany w pliku project-vision.md

-Ulepsz następujący prompt [ID prompta], uwzględniając [nowe wymagania]:

[treść poprzedniego prompta]
[zmiany w pliku project-vision.md]

-Prompt nie ma być zbyt złożony aby nie zajmował zbyt wiele czasu agentowi i nie był zbyt skomplikowany. Możesz odejmować i modyfikować elementy poprzednich wersji wg. uznania.

-Prompt ma być czytelny i spójny.

-Stwórz dokumentację dla następującego promptu, uwzględniając jego historię wersji:

[treść promptu]
[lista zmian w wersjach]

-Po zakończeniu generowania, podpisz swoją odpowiedź aktualną nazwą modelu i datą.

-Upewnij się że zastosowano listę kontrolną jak w szablonie prompt-template.md:

> (źródło: prompt-template.md)
>
> - [ ] Prompt jest jednoznaczny i spójny
> - [ ] Instrukcje są precyzyjne
> - [ ] Format wyniku jest jasno określony
> - [ ] Zgodność z prompt-rules.md
> - [ ] Zgodność z workflow.md

-Zsynchronizuj historię wersji prompta z głównym plikiem prompta prompt.md o ID takim samym jak nazwa jego folderu. Tj. ostatnia wygenerowana wersja prompta musi się zgadzać z prompt.md z głównego folderu prompta.

## Formatowanie treści zewnętrznych

Przy włączaniu treści z zewnętrznych plików (np. project-vision.md) do promptów:

1. Zawsze poprzedzaj blok treści zewnętrznej jasnym nagłówkiem lub adnotacją wskazującą źródło, np. `### Wizja projektu (treść z project-vision.md)` lub `> (źródło: architecture.md)`.
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
