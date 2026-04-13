# Błędy Poznawcze i Modele Ekonomiczne

> Źródło: [fs.blog/mental-models](https://fs.blog/mental-models/)

Świadomość błędów poznawczych jest warunkiem koniecznym do skutecznego stosowania innych modeli myślowych. Bez niej łatwo stosujemy narzędzia do potwierdzania tego, w co już wierzymy.

---

## BŁĘDY POZNAWCZE (Cognitive Biases)

### Błąd Potwierdzenia (Confirmation Bias)

Naturalny mechanizm, przez który aktywnie szukamy informacji potwierdzających nasze istniejące przekonania, a ignorujemy lub odrzucamy te, które im przeczą.

**Dlaczego to ważne:** To jeden z najgroźniejszych błędów, bo jest niewidoczny z wewnątrz. Badamy tylko to, co chcemy udowodnić, i konstruujemy argumenty wokół z góry przyjętej tezy.

**Przeciwdziałanie:** Aktywne szukanie dowodów obalających własne hipotezy. Zamiast pytać „Czy to prawda?", pytaj „Co musiałoby być prawdą, żebym się mylił?".

**W pracy z LLM:** Model językowy wzmacnia confirmation bias — generuje odpowiedzi pasujące do framingu pytania. Celowo konstruuj pytania z przeciwnej strony.

---

### Heurystyka Dostępności (Availability Heuristic)

Oceniamy prawdopodobieństwo i istotność zdarzeń na podstawie tego, jak łatwo przychodzą nam do głowy — nie na podstawie rzeczywistych danych.

**Przykład:** Po katastrofie lotniczej w mediach ludzie boją się latać bardziej niż prowadzić samochód — choć statystycznie samochód jest wielokrotnie bardziej niebezpieczny. Katastrofa jest łatwo dostępna w pamięci.

**Zastosowanie:** Nie ufaj intuicji w ocenie ryzyka bez danych. To, co głośne, widowiskowe i niedawne, będzie zawsze nadreprezentowane w naszej ocenie rzeczywistości.

---

### Błąd Utopionych Kosztów (Sunk Cost Fallacy)

Kontynuowanie inwestycji (czasu, pieniędzy, energii) wyłącznie dlatego, że już dużo zainwestowaliśmy — niezależnie od obecnych i przyszłych perspektyw.

**Dlaczego to pułapka:** Minione koszty są nieodwracalne. Jedynym kryterium decyzji powinny być przyszłe koszty i korzyści — nie to, ile już włożyliśmy.

**Przykłady:** Kontynuowanie złego projektu „bo tyle czasu w to włożyliśmy", trwanie w niedziałającym związku, dosiadanie się do złej inwestycji giełdowej.

**Pytanie korygujące:** „Gdybym zaczynał od zera dziś — czy bym to kontynuował?"

---

### Błąd Narracyjny (Narrative Fallacy)

Umysł ludzki jest maszyną do tworzenia spójnych historii. Nadajemy sens zdarzeniom post factum, tworząc narracje przyczynowo-skutkowe, nawet gdy zdarzenia były przypadkowe.

**Dlaczego to groźne:** Opowieści są przekonujące i łatwe do zapamiętania — ale upraszczają, ignorują przypadek i nadają fałszywe poczucie przewidywalności.

**Zastosowanie:** Bądź podejrzliwy wobec zbyt pięknych, spójnych historii sukcesu. Sukces często ma więcej wspólnego z warunkami zewnętrznymi i szczęściem niż z konkretną decyzją bohatera narracji.

---

### Efekt Zakotwiczenia (Anchoring Effect)

Pierwsze dane, które otrzymujemy, służą jako „kotwica" — punkt odniesienia, do którego nieświadomie dostosowujemy wszystkie późniejsze oceny.

**Przykład:** Jeśli negocjator poda wysoką cenę wyjściową, ostateczna cena będzie wyższa, niż gdyby zaczął od niższej — nawet jeśli obie strony „negocjowały uczciwie".

**Zastosowanie:** Zawsze sprawdzaj, skąd pochodzi pierwsza liczba lub ocena. W pracy z LLM: framing promptu ustala kotwicę dla całej odpowiedzi modelu.

---

### Pewność Wsteczna (Hindsight Bias)

Po tym jak zdarzenie nastąpiło, wydaje nam się, że „wiedzieliśmy to od początku". Zjawisko zniekształca uczenie się na błędach — bo trudno odtworzyć, co naprawdę wiedzieliśmy przed faktem.

**Dlaczego to ważne:** Utrudnia uczciwe wyciąganie wniosków. Jeśli po każdej porażce mówimy „mogłem to przewidzieć" — nie poprawiamy procesu decyzyjnego, tylko poprawiamy sobie samopoczucie.

---

## MODELE EKONOMICZNE

### Zachęty (Incentives)

Charlie Munger nazywał incentives „supermocą". Pokaż mi zachęty, a pokażę ci zachowanie.

**Zasada:** Ludzie reagują na incentives — często bardziej niż na własne deklaracje, wartości czy instrukcje. Jeśli system nagradzania jest zły, dobre wyniki są przypadkowe.

**Zastosowanie:** Przy projektowaniu systemów i ocenie cudzych zachowań — zawsze pytaj: jakie incentives są tutaj aktywne? Kto zyska, jeśli sprawa pójdzie w dany sposób?

**Pułapka:** Własne incentives są najtrudniejsze do dostrzeżenia — właśnie dlatego warto łączyć ten model z inwersją.

---

### Koszty Okazji (Opportunity Costs)

Koszt każdej decyzji to nie tylko to, co płacimy — to też najlepsza rzecz, z której rezygnujemy, podejmując tę decyzję. Każde „tak" to jednocześnie wiele „nie".

**Zastosowanie:** Oceniaj decyzje nie tylko przez pryzmat bezpośrednich kosztów i korzyści, ale też przez to, co tracisz. Szczególnie ważne przy alokacji czasu — najtrudniejszego zasobu do odzyskania.

---

### Wąskie Gardła (Bottlenecks / Theory of Constraints)

W każdym systemie istnieje jeden czynnik limitujący, który ogranicza całkowitą przepustowość. Poprawa czegokolwiek poza wąskim gardłem nie zwiększa ogólnej wydajności systemu.

**Zastosowanie:** Zanim zoptymalizujesz cokolwiek — znajdź wąskie gardło. Teoria Ograniczeń (Goldratt): skoncentruj wysiłek na wąskim gardle, resztę systemu puść luzem.

**W pracy z LLM:** Wąskim gardłem rzadko jest model — częściej jakość danych wejściowych, framing pytania lub brak weryfikacji wyników.

---

### Regresja do Średniej (Regression to the Mean)

Skrajne wyniki — zarówno bardzo dobre, jak i bardzo złe — mają naturalną tendencję do zbliżania się do średniej przy kolejnych pomiarach. Nie dlatego, że coś się zmieniło, ale dlatego, że skrajne wyniki częściowo zawdzięczają swoje istnienie szczęściu.

**Pułapka:** Mylenie powrotu do średniej z efektem interwencji. Pracownik, który miał bardzo zły tydzień i dostał reprymendę, może następny mieć lepszy — nie dlatego, że reprymenda zadziałała, ale dlatego, że zły tydzień był częściowo przypadkowy.

---

*Powrót do [indeksu](index.md)*
