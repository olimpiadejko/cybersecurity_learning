# Introduction to Cybersecurity

## Red Team (Offensive Security)
Bezpieczeństwo ofensywne polega na symulowaniu działań hakera i wyszukiwaniu słabych punktów zanim zrobią to prawdziwi atakujący.

### Pentesting
Testy penetracyjne (pentesting) polegają na szukaniu luk w zabezpieczeniach, aby sprawdzić, czy potencjalny haker mógłby je wykorzystać.  
Wyniki takich testów pomagają firmom zrozumieć zagrożenia i naprawić błędy zanim zostaną wykorzystane.

---

## Przykład podatności (ukryte strony)
Częstym błędem jest pozostawianie ukrytych stron dostępnych publicznie.

### Narzędzie: dirb
- wyszukuje ukryte zasoby i katalogi
- wpisy zaczynające się od "+" oznaczają znalezione ścieżki

Jeśli taka ścieżka zostanie wpisana w przeglądarce, można uzyskać dostęp do części strony, które nie powinny być publiczne.

---

## Blue Team (Defensive Security)
Bezpieczeństwo obronne polega na ochronie systemów i reagowaniu na zagrożenia.

Obejmuje:
- wykrywanie ataków
- analizę incydentów
- reagowanie na zagrożenia

Celem jest zatrzymanie ataku zanim spowoduje szkody.

---

## My notes / What I learned
- Istnieją dwa główne podejścia: Red Team (atak) i Blue Team (obrona)
- Pentesting pomaga znaleźć luki zanim zrobi to prawdziwy atakujący
- Nawet proste błędy (np. ukryte strony) mogą prowadzić do poważnych problemów
- Narzędzia takie jak dirb pozwalają wykrywać ukryte zasoby
