# Cryptography Basics

## Basic Concepts

### Plaintext
Plaintext (tekst jawny) to zwykła, czytelna wiadomość przed zaszyfrowaniem.

Przykład:
- "Hello"

---

### Ciphertext
Ciphertext (szyfrogram) to wiadomość po zaszyfrowaniu.

Przykład:
- "Khoor"

Wygląda bez sensu bez odpowiedniego klucza.

---

### Key
Klucz to sekret używany do szyfrowania i/lub odszyfrowania danych.

---

### Algorithm
Algorytm to „przepis” określający sposób szyfrowania.

Przykład:
- Szyfr Cezara:
przesuń każdą literę o X pozycji.

Algorytm może być publiczny.

---

## Encryption Process

Szyfrowanie:

```text
Plaintext + Key + Algorithm → Ciphertext
```

Deszyfrowanie:

```text
Ciphertext + Key + Algorithm → Plaintext
```

---

## Caesar Cipher

Prosty historyczny szyfr.

Dla klucza = 3:

```text
ABC → DEF
```

Odszyfrowanie:
- przesunięcie w przeciwną stronę.

---

## Kerckhoffs’s Principle

System powinien być bezpieczny nawet jeśli przeciwnik zna algorytm.

Bezpieczeństwo ma zależeć od tajności klucza, a nie ukrywania sposobu działania.

---

# Symmetric Encryption

Szyfrowanie symetryczne:

- ten sam klucz służy do szyfrowania i odszyfrowania

```text
Shared Secret Key
```

## Problem:
Dystrybucja klucza

Jak bezpiecznie przekazać klucz drugiej stronie?

To klasyczny problem symmetric cryptography.

---

# Asymmetric Encryption

Rozwiązuje problem dystrybucji kluczy.

Każdy użytkownik ma dwa klucze:

## Public Key
- dostępny dla wszystkich  
- służy do szyfrowania

---

## Private Key
- zna go tylko właściciel  
- służy do odszyfrowania

---

Przykład:

Alice szyfruje wiadomość kluczem publicznym Boba.

Tylko Bob może odszyfrować ją swoim kluczem prywatnym.

---

## Analogia

Public key:
- jak numer konta lub skrzynka pocztowa

Private key:
- jak PIN lub klucz do skrzynki

---

# Hybrid Encryption

W praktyce używa się połączenia obu metod:

1. Asymmetric crypto  
- uzgadnia bezpiecznie klucz

2. Symmetric crypto  
- szyfruje całą dalszą komunikację

to podejście hybrydowe.

---

# HTTPS / TLS

To najpopularniejsze użycie kryptografii asymetrycznej.

Podczas połączenia:

1. przeglądarka żąda klucza publicznego serwera

2. serwer wysyła:
- public key  
- certyfikat

---

## Certificate

Certyfikat zawiera:
- klucz publiczny
- właściciela domeny
- podpis CA (Certificate Authority)

Przeglądarka sprawdza:
- czy CA jest zaufany
- czy certyfikat jest ważny

---

## Session Key

Po weryfikacji obie strony uzgadniają wspólny klucz symetryczny (session key).

Od tej chwili komunikacja używa szyfrowania symetrycznego, bo jest szybsze.

---

## Check Certificate

Klikając ikonę kłódki w przeglądarce można sprawdzić:
- ważność certyfikatu
- wystawcę
- szczegóły szyfrowania

---

## My notes / What I learned

- plaintext to dane przed szyfrowaniem  
- ciphertext to dane po szyfrowaniu  
- symmetric encryption używa jednego klucza  
- asymmetric encryption używa public/private key  
- HTTPS wykorzystuje podejście hybrydowe  
- bezpieczeństwo zależy od klucza, nie tajności algorytmu  
