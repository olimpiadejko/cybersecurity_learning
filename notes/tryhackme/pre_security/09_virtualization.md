# Virtualization

## What is virtualization?
Wirtualizacja to technologia, która pozwala uruchomić wiele niezależnych systemów operacyjnych na jednym fizycznym komputerze (serwerze).

Każda maszyna wirtualna działa jak osobny komputer:
- posiada własny system operacyjny  
- ma własne aplikacje  
- ma własne ustawienia  
- jest odizolowana od innych  

---

## Hypervisor

Hiperwizor to oprogramowanie, które zarządza wirtualizacją.

Jego zadania:
- zarządzanie zasobami (CPU, RAM, dysk)  
- dzielenie zasobów między maszyny wirtualne  
- izolowanie maszyn od siebie  
- umożliwienie ich niezależnego działania  

działa jako „pośrednik” między sprzętem a VM

---

## How virtualization works (step by step)

1. Mamy fizyczny komputer (serwer)  
2. Instalujemy hiperwizor  
3. Tworzymy maszyny wirtualne (VM)  
4. Instalujemy na nich systemy operacyjne  
5. Każda VM działa jak oddzielny komputer  

---

## Use in Cybersecurity

- **Izolacja** → atak na jedną VM nie wpływa na inne  
- **Bezpieczne testy** → można testować malware i exploity  
- **Środowiska labowe** → nauka i praktyka  
- **Snapshoty** → cofnięcie systemu do wcześniejszego stanu  

---

## Virtual Machine (VM)

Maszyna wirtualna to wirtualny komputer tworzony przez hiperwizor.

Cechy:
- posiada wirtualny CPU, RAM, dysk i sieć  
- można zainstalować dowolny system (Windows, Linux)  
- działa niezależnie od innych VM  

jest w pełni izolowana, ale zużywa więcej zasobów  

### Zastosowania:
- testowanie systemów (np. Kali Linux)  
- analiza malware  
- laby cyberbezpieczeństwa  

---

## Containers

Kontener to lekkie środowisko do uruchamiania aplikacji.

Cechy:
- zawiera aplikację i zależności  
- współdzieli system operacyjny hosta (ten sam kernel)  
- nie posiada własnego OS  
- uruchamia się bardzo szybko  
- zużywa mało zasobów  

izolacja jest słabsza niż w VM  

---

## Docker

Docker to najpopularniejsze narzędzie do kontenerów.

Umożliwia:
- tworzenie kontenerów  
- uruchamianie aplikacji  
- łatwe przenoszenie środowisk  

---

## VM vs Containers (difference)

- VM → pełny system operacyjny, większe zużycie zasobów  
- Container → lekki, szybki, współdzieli system  

---

## Example Use Cases

### Virtual Machines:
- uruchamianie innych systemów (np. Kali Linux)  
- testowanie wirusów  
- nauka cyberbezpieczeństwa  

### Containers:
- uruchamianie aplikacji w identycznym środowisku  
- development i testy  
- wdrożenia (deploy) aplikacji  

---

## My notes / What I learned
- wirtualizacja pozwala uruchomić wiele systemów na jednym sprzęcie  
- hiperwizor zarządza zasobami i izolacją  
- VM są bezpieczniejsze, ale cięższe  
- kontenery są szybsze i lżejsze  
- w cybersec VM są kluczowe do testów i nauki  
