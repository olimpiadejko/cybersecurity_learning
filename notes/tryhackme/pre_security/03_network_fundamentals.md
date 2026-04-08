# Network Fundamentals (LAN, Subnetting, ARP, DHCP)

## LAN Topologies

Topologia sieci LAN określa, jak urządzenia są połączone ze sobą.

---

### Star Topology (Gwiazda)

- wszystkie urządzenia podłączone do jednego centralnego urządzenia (switch/hub)  
- dane przechodzą przez switch (nie bezpośrednio)  

Zalety:
- łatwa rozbudowa (skalowalność)  
- awaria jednego urządzenia nie psuje całej sieci  

Wady:
- więcej kabli = wyższy koszt  

---

### Bus Topology (Magistrala)

- wszystkie urządzenia podłączone do jednego kabla (backbone)  

Jak działa:
- dane „lecą” wzdłuż kabla  
- wszystkie urządzenia je widzą  
- tylko właściwy odbiorca je odbiera  

Zalety:
- tania  
- prosta  

Wady:
- wąskie gardło (bottleneck)  
- przerwanie kabla = cała sieć nie działa  

---

### Ring Topology (Pierścień)

- urządzenia tworzą zamkniętą pętlę  
- każde urządzenie ma dwóch sąsiadów  

Jak działa:
- dane lecą w jednym kierunku  
- każde urządzenie przekazuje dane dalej  

Zalety:
- mało okablowania  

Wady:
- przerwanie kabla = cała sieć przestaje działać  

---

## Network Devices

### Switch

Switch łączy urządzenia w jednej sieci LAN.

- zapamiętuje, które urządzenie jest pod którym portem  
- wysyła dane tylko tam gdzie trzeba (nie do wszystkich jak hub)  

większa wydajność i mniej ruchu  

---

### Router

Router łączy różne sieci ze sobą.

- używa routingu (tworzenie ścieżek)  
- najczęściej: sieć domowa ↔ internet  

---

## Subnetting

Subnetting to dzielenie jednej sieci na mniejsze.

Dlaczego?
- lepsza organizacja  
- mniejszy chaos  
- większa kontrola  

---

### IP Address Structure

Adres IP składa się z:
- części sieci (network)  
- części hosta (device)  

---

### Subnet Mask

Maska podsieci określa podział.

Przykład:
IP: 192.168.1.100  
Maska: 255.255.255.0  

- 255 → część sieci  
- 0 → część hosta  

pierwsze 3 liczby = sieć  
ostatnia = host  

---

### Same Network

Dwa urządzenia są w tej samej sieci, jeśli:
- mają tę samą część sieciową  

wtedy mogą komunikować się bez routera  

---

## ARP (Address Resolution Protocol)

ARP służy do znalezienia adresu MAC na podstawie IP.

Jak działa:
1. wysyłany jest ARP Request (do całej sieci)  
2. urządzenie z danym IP odpowiada (ARP Reply)  
3. zwraca swój adres MAC  

zapis w ARP Cache (na przyszłość)  

---

## DHCP (Dynamic Host Configuration Protocol)

DHCP automatycznie przydziela adresy IP.

---

### DHCP Process

1. **Discover** → klient szuka IP  
2. **Offer** → serwer proponuje IP  
3. **Request** → klient akceptuje  
4. **ACK** → serwer zatwierdza  

---

Po tym:
- dostajesz IP  
- maskę podsieci  
- gateway (router)  
- DNS  

możesz korzystać z internetu  

---

## My notes / What I learned
- topologia określa strukturę sieci  
- switch działa inteligentnie, hub nie  
- router łączy różne sieci  
- subnetting dzieli sieć na mniejsze części  
- ARP tłumaczy IP → MAC  
- DHCP automatycznie przydziela IP  
