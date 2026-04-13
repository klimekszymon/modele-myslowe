# Modele Myślowe w Pracy z LLM

> Źródło: [fs.blog/mental-models](https://fs.blog/mental-models/) + notatki własne

Stosowanie modeli myślowych w pracy z LLM pozwala przejść od chaotycznego „rozmawiania" z AI do systematycznego, inżynieryjnego podejścia. Modele mentalne można traktować jak wzorce projektowe dla procesów poznawczych.

---

## 1. Myślenie z Pierwszych Zasad (First Principles Thinking)

**Cel:** Dekonstrukcja skomplikowanych problemów do poziomu fundamentalnych faktów, aby budować rozwiązania od zera — bez polegania na utartych, często przestarzałych schematach. Zapobiega powielaniu przez model standardowego, ale nieoptymalnego boilerplate'u.

**Kiedy użyć:** Gdy LLM nie radzi sobie z zadaniem „z pudełka". Zamiast dawać ogólne polecenie, rozbij problem na podstawowe prawdy (wejście danych, oczekiwany algorytm, ograniczenia pamięciowe) i każ modelowi budować rozwiązanie od tych fundamentów.

**Kluczowe cechy:**
- Redukcjonizm
- Ignorowanie status quo
- Budowanie logiki od fundamentów
- Dociekanie prawdziwych przyczyn problemu (np. wąskich gardeł wydajnościowych)

**Tagi:** `#Dekompozycja` `#Fundamenty` `#Architektura` `#Innowacja`

---

## 2. Inwersja (Inversion)

**Cel:** Odwrócenie perspektywy problemu, aby zidentyfikować, co może pójść nie tak. Zamiast szukać idealnego rozwiązania — skup się na wyeliminowaniu ścieżek prowadzących do błędu. Świetnie sprawdza się do audytowania kodu wygenerowanego przez AI.

**Kiedy użyć:** Zamiast pytać „Jak napisać ten komponent w Vue?", zapytaj „Jakie błędy w implementacji tego komponentu sprawią, że będzie on niewydajny lub niebezpieczny?". Model zidentyfikuje potencjalne pułapki przed napisaniem właściwego kodu.

**Kluczowe cechy:**
- Myślenie „od tyłu"
- Unikanie porażek zamiast pogoni za sukcesem
- Proaktywna identyfikacja zagrożeń technicznych

**Tagi:** `#Prewencja` `#Debugowanie` `#Antywzorce` `#RedukcjaBłędów`

---

## 3. Myślenie Drugiego Rzędu (Second-Order Thinking)

**Cel:** Wykraczanie poza natychmiastowe efekty zaproponowanego przez AI rozwiązania i przewidywanie jego długofalowych konsekwencji. Wymusza zadawanie pytania „I co potem?".

**Kiedy użyć:** Gdy AI proponuje rozwiązanie z użyciem konkretnego pakietu — zbadaj, jak wpłynie to za kilka miesięcy na bundle size, dług technologiczny czy skalowanie projektu.

**Kluczowe cechy:**
- Długoterminowa perspektywa
- Analiza skutków ubocznych (efekt domina)
- Myślenie systemowe w architekturze IT

**Tagi:** `#Konsekwencje` `#DługTechnologiczny` `#Skalowalność` `#AnalizaRyzyka`

---

## 4. Brzytwa Ockhama (Occam's Razor)

**Cel:** Bezwzględne eliminowanie zbędnej złożoności w kodzie i w promptach. Jeśli LLM generuje nadmiernie skomplikowany komponent lub abstrakcję — wymuś na nim najprostsze działające rozwiązanie z minimalną liczbą zależności.

**Kiedy użyć:** Gdy prompt staje się zbyt długi i model zaczyna się gubić — usuń zbędne instrukcje. Jeśli wygenerowany kod jest zbyt skomplikowany — wymuś uproszczenie.

**Kluczowe cechy:**
- Prostota i minimalizm w kodzie
- Odrzucanie zbędnych założeń
- Poszukiwanie najkrótszej drogi do celu

**Tagi:** `#Minimalizm` `#Optymalizacja` `#CzystyKod` `#Refaktoryzacja`

---

## 5. Myślenie Probabilistyczne (Probabilistic Thinking)

**Cel:** Trafna ewaluacja wyników LLM poprzez traktowanie ich jako prawdopodobieństwa, a nie absolutnej prawdy. Modele językowe to w dużej mierze silniki statystyczne — ten model uodparnia na zjawisko halucynacji.

**Kiedy użyć:** Zawsze przy krytycznych zadaniach. Traktuj każdą odpowiedź jako „prawdopodobnie poprawną", a nie fakt. Używaj parametrów `top_p` i `temperature`, aby kontrolować losowość podczas researchu.

**Kluczowe cechy:**
- Praca z niepewnością
- Szacowanie ryzyka błędu
- Ciągłe aktualizowanie zaufania na podstawie wyników
- Testowanie wielowariantowe (generowanie kilku wersji kodu i ich porównanie)

**Tagi:** `#OcenaRyzyka` `#Ewaluacja` `#ZarządzanieNiepewnością` `#ŚwiadomośćHalucynacji`

---

## 6. Krąg Kompetencji (Circle of Competence)

**Cel:** Jasne zdefiniowanie granic wiedzy — zarówno Twoich własnych, jak i modelu AI. Pomaga określić, kiedy możesz w pełni polegać na wygenerowanym kodzie, a kiedy powinieneś zachować skrajny sceptycyzm.

**Kiedy użyć:**
- Pełne zaufanie: dobrze udokumentowane wzorce TypeScript, standardowy boilerplate
- Skrajny sceptycyzm + fact-checking: nowe API po dacie odcięcia wiedzy modelu, niszowe konfiguracje

**Kluczowe cechy:**
- Samoświadomość ograniczeń
- Określanie granic zaufania do asystenta AI
- Granie tam, gdzie masz przewagę weryfikacyjną

**Tagi:** `#GraniceWiedzy` `#Weryfikacja` `#FactChecking` `#Zaufanie`

---

## 7. Mapa to nie Terytorium (The Map is Not the Territory)

**Cel:** Przypomnienie, że wiedza „wbudowana" w model AI (mapa) nigdy nie odzwierciedla w pełni aktualnej, działającej rzeczywistości produkcyjnej (terytorium). Wymusza nawyk dostarczania modelowi brakującego i aktualnego kontekstu.

**Kiedy użyć:** Zawsze przy pracy z bibliotekami lub API, które mogły się zmienić. Dostarczaj modelowi najnowszą dokumentację, logi błędów środowiska lub specyfikację wewnętrznego API poprzez RAG lub wklejenie w prompt.

**Kluczowe cechy:**
- Świadomość nieaktualności wiedzy bazowej modelu
- Rozróżnienie wygenerowanej teorii od środowiska wykonawczego
- Nacisk na twardy, aktualny kontekst

**Tagi:** `#OgraniczeniaKontekstu` `#WiedzaZdezaktualizowana` `#Grounding` `#RAG`

---

## Tabela podsumowująca

| Model | Główne zastosowanie w LLM | Kluczowe pytanie |
|-------|--------------------------|-----------------|
| Pierwsze zasady | Dekompozycja złożonych promptów | „Jakie są fundamentalne fakty?" |
| Inwersja | Redukcja halucynacji i błędów | „Co może pójść nie tak?" |
| Myślenie 2. rzędu | Architektura systemów AI | „I co potem?" |
| Brzytwa Ockhama | Optymalizacja promptów, czysty kod | „Czy mogę to uprościć?" |
| Myślenie probabilistyczne | Ewaluacja odpowiedzi | „Jak pewna jest ta odpowiedź?" |
| Krąg kompetencji | Fact-checking | „Czy mogę tu ufać modelowi?" |
| Mapa vs. terytorium | Rozumienie ograniczeń modelu | „Czy wiedza modelu jest aktualna?" |

---

*Powrót do [indeksu](readme.md)*
