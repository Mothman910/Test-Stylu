project-name/
├── README.md # Podstawowe informacje o projekcie
├── .gitignore # Lista ignorowanych plików
├── docs/ # Dokumentacja
│ ├── architecture.md # Opis architektury
│ ├── api.md # Dokumentacja API
│ ├── prompts/ # Katalog na prompty AI
│ │ ├── feature-a/
│ │ │ ├── prompt.md # Aktualny prompt
│ │ │ └── history/ # Historia wersji
│ │ │ ├── v1.0.md
│ │ │ ├── v2.0.md
│ │ │ └── v3.0.md
│ │ ├── feature-b/
│ │ │ ├── prompt.md
│ │ │ └── history/
│ │ ├── project-init/
│ │ │ ├── prompt.md
│ │ │ └── history/
│ │ ├── examples/
│ │ │ ├── project-init/ # Przykład rozpoczęcia pracy nad promptami
│ │ │ │ ├── prompt.md
│ │ │ │ └── history/
│ │ │ │ ├── v1.0.md
│ │ │ │ └── v2.0.md
│ │ │ └── feature-a/ # Przykład generowania kolnego prompta dla agenta AI
│ │ │ ├── prompt.md
│ │ │ └── history/
│ │ └── metadata.md # Informacje o modelach i strategiach
│ └── tutorials/ # Poradniki
├── src/ # Kod źródłowy
├── tests/ # Testy
└── data/ # Dane (często z .gitignore)
