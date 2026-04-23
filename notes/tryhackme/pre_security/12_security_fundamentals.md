# Security Fundamentals

## CIA Triad

CIA Triad to trzy filary cyberbezpieczeństwa:

### Confidentiality (Poufność)
Poufność oznacza, że tylko uprawnione osoby mają dostęp do danych.

Przykład:
- hasło do banku powinien znać tylko właściciel konta

Jeśli poufność zostanie naruszona:
- wyciek danych  
- naruszenie prywatności  
- straty finansowe  
- konsekwencje prawne  

---

### Integrity (Integralność)
Integralność oznacza, że dane nie powinny zostać zmodyfikowane przez nieuprawnione osoby.

Jeśli integralność zostanie naruszona:
- dane stają się niewiarygodne  
- mogą prowadzić do błędnych decyzji  

Przykład:
- zmiana kwoty przelewu przez atakującego

---

### Availability (Dostępność)
Dane i systemy powinny działać wtedy, gdy są potrzebne.

Przykłady naruszenia:
- awaria systemu  
- atak DDoS  
- ransomware

---

Większość ataków celuje w jeden lub więcej elementów CIA.

---

## Common Weaknesses

## Weak Authentication

Uwierzytelnianie może opierać się na:

### Something you know
- hasło  
- PIN

### Something you are
- odcisk palca  
- Face ID

### Something you have
- telefon do odbioru kodu SMS  
- token

---

## Weak Passwords

Słabe hasła zagrażają poufności.

Problemy:
- proste hasła (np. qwerty)  
- używanie tego samego hasła wszędzie  

### Credential Stuffing
Atakujący bierze wyciekłe hasło i próbuje je na wielu serwisach.

---

## Weak File Permissions

Złe uprawnienia mogą umożliwić dostęp do plików osobom nieuprawnionym.

Zasada:
- użytkownik powinien mieć tylko taki dostęp, jakiego potrzebuje

(Principle of Least Privilege)

---

## Malware

Złośliwe oprogramowanie może atakować:
- Confidentiality  
- Integrity  
- Availability

---

### Trojan

Koń trojański może:
- dać atakującemu dostęp do systemu  
- umożliwić odczyt lub modyfikację plików

Atakuje głównie poufność.

---

### Ransomware

Ransomware szyfruje pliki i blokuje dostęp.

Skutek:
- naruszenie dostępności

Atakujący żąda okupu za odzyskanie danych.

---

# Basic Linux Attack Simulation (TryHackMe Lab)

## SSH Login

Przykład zdalnego logowania:

```bash
ssh sammie@10.114.158.148
```

Możliwy atak:
- password guessing attack

---

## Enumeration

Po uzyskaniu dostępu zbieramy informacje:

- przegląd plików  
- szukanie haseł  
- analiza konfiguracji  

---

## Password Reuse

Sprawdzanie, czy poznane hasło działa dla innych kont.

---

## Command History

Polecenie:

```bash
history
```

Może ujawnić:
- hasła wpisane przez nieuwagę  
- komendy administratora

---

## Privilege Escalation

Próba zdobycia wyższych uprawnień aż do root.

### Root

W Linux/macOS:
- konto administratora z pełnym dostępem

W Windows odpowiednik:
- Administrator

---

## My notes / What I learned

- CIA Triad to fundament cyberbezpieczeństwa  
- słabe hasła i złe uprawnienia tworzą luki  
- malware może atakować różne elementy CIA  
- enumeracja i privilege escalation są częścią ataków post-exploitation  
