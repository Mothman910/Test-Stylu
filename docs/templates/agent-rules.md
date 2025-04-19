# Reguły do stosowania przez Agentów AI przy pracy nad projektem:

## 1. Umieszczanie wygenerowanego kodu:

1. Zapisuj kod wygenerowany przez prompt w odpowiednich plikach projektu z uwzględnieniem już istniejących.
2. Sprawdz czy istnieją i wykorzystuj już istniejące pliki i foldery zanim przystąpisz do utworzenia nowych.
3. Staraj się nie dublować plików projektu i umieszczać je w odpowiednich folderach
4. Dodawaj komentarz z referencją do promptu: // Wygenerowano przez prompt: docs/prompts/feature-name/prompt.md
5. W trybie Agenta nie zmieniaj plików zapisanych w folderach /docs/prompts i /docs/templates projektu. Chce na nich pracować tylko w trybie Zapytania lub Edycji.
6. Nie umieszczaj komentarzy w plikach formatu .json (nie są dozwolone i generują błędy)

## 2. Praca z terminalem

7. Nie używaj operatora && w terminalu gdyż pracujemy w konsoli PowerShell Windows 11 !important
8. Nie twórz zagnieżdżonej struktury folderów projektu. Szablony projektów Aplikacji z komend takich jak:

```console
$ npx @react-native-community/cli init .
```

instaluj w głównym folderze projektu.
