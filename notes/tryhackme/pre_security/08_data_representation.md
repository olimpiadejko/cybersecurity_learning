# Data Representation (RGB & Encoding)

## RGB Color Model

### Basics
Kolory w komputerze tworzone są z trzech składowych:
- **R** (Red)  
- **G** (Green)  
- **B** (Blue)  

---

### Binary Model (0/1)

Każdy kolor może być:
- 0 → wyłączony  
- 1 → włączony  

Liczba kombinacji:
2 × 2 × 2 = 8 kolorów  

Przykłady:
- 000 → czarny  
- 001 → niebieski  
- 010 → zielony  
- 100 → czerwony  
- 111 → biały  

Bit = pojedyncza wartość (0 lub 1)

---

### Full Color Range

Każdy kanał (R, G, B):
- 256 poziomów (0–255)

Łączna liczba kolorów:
256 × 256 × 256 = 16,777,216  

---

### Bits and Bytes

- 1 bajt = 8 bitów  
- 1 kolor (R/G/B) = 1 bajt  
- cały kolor = 3 bajty = 24 bity  

---

### HEX Representation

- 4 bity = 1 znak HEX  
- znaki: 0–9, A–F  

Przykład:
10100011 11101010 00101010 → A3EA2A  

- 1 bajt = 2 znaki HEX  
- kolor = 6 znaków HEX  

Format:
#RRGGBB (np. #A3EA2A)  

---

## Data Encoding

### What is encoding?
Kodowanie to przypisanie liczb do znaków.

Przykłady:
- 65 → 'A'  
- 97 → 'a'  
- 33 → '!'  

Tekst = ciąg liczb  

Przykład:
"Kot" → 75 111 116  

---

### Encoding Problem

Jeśli tekst zostanie zapisany w jednym kodowaniu, a odczytany w innym:
- dane zostaną źle zinterpretowane  
- pojawiają się „krzaczki”  

---

### ASCII

ASCII to system kodowania znaków:
- zakres: 0–127  
- brak obsługi polskich znaków i emoji  

Powstały rozszerzenia:
- ISO-8859-1  
- ISO-8859-2  

problem: różne wersje = niekompatybilność  

---

### Unicode

Unicode przypisuje unikalny numer każdemu znakowi.

- ~157 000 znaków  
- obsługuje wszystkie języki + emoji  

---

### UTF Encodings

#### UTF-8
- 1–4 bajty  
- kompatybilny z ASCII  
- oszczędny  
- najczęściej używany (HTML, API)  

---

#### UTF-16
- 2–4 bajty  
- większość znaków = 2 bajty  
- mniej efektywny dla prostych tekstów  

---

#### UTF-32
- zawsze 4 bajty  
- bardzo duże zużycie pamięci  
- rzadko używany  

---

## My notes / What I learned
- kolory w komputerze opierają się na RGB i bitach  
- HEX to sposób zapisu kolorów używany w webie  
- tekst to tak naprawdę liczby  
- różne kodowania mogą powodować błędy  
- Unicode rozwiązuje problem wielu języków  
- UTF-8 to standard w nowoczesnych systemach  
