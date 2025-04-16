# Zadatak iz Softverske Metrike

## LOC (Lines of Code)

Ovo su izracunate linije za sve fajlove u projektu:

| Fajl            | Ukupno linija | LOC (efektivni kod) |
|------------------|----------------|------------------------|
| Calculator.java   | 143            | 118                    |
| Start.java        | 28             | 24                     |
| LICENSE           | 21             | 0                      |
| **Ukupno**        | **192**        | **142**                |

Napomena: LOC se odnosi samo na stvarne linije koda, bez praznih linija i komentara.

---

## Staticka analiza i zapažanja

### Fajl: `Calculator.java`
- Linija 6 – Koriscenje statičke promenljive `finalResult` može izazvati probleme ako se koristi vise niti.
- Linija 11 – Metoda `ToString()` nije po Java konvenciji (`toString()`), može zbuniti.
- Linija 29 – Dodavanje nule na pocetak izraza može biti neintuitivno, ali resava problem izraza koji pocinju znakom.
- Linija 35 – Petlja ne uzima u obzir poslednji karakter, moze preskociti operaciju.
- Linije 68–142 – Funkcija `Calculate()` je dosta duga i kompleksna, možda bi trebalo podeliti u manje funkcije.
- Opšti komentar – Nema komentara kroz kod, što otežava razumevanje.

### Fajl: `Start.java`
- Linija 10 – Scanner se pravi unutar petlje, bolje bi bilo da se definiše van nje.
- Linija 20 – Nedostaje provera ispravnosti izraza koji korisnik unosi, može doći do greske.

---

## Zakljucak

Kod je funkcionalan i radi osnovne operacije kalkulatora, ali postoje mesta koja mogu da se poboljsaju. Posebno bi pomoglo dodavanje komentara i jednostavnije razdvajanje funkcionalnosti u manje metode. Takodje, mozze se unaprediti rad sa korisnickim unosom.
