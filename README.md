# System Centralny dla Firmy Dealerskiej

## Projekt Systemu Centralnego

### Wykonawcy:
- Adam Czerwiec
- Adam Cypliński
- Bartłomiej Gromek

### Kierunek studiów:
Elektronika i Telekomunikacja 2023/2024

## Cel Projektu

Celem projektu było stworzenie systemu centralnego dla firmy dealerskiej, dostosowanego do struktury organizacyjnej firmy. System obejmuje oddziały takie jak: księgowość, logistyka, marketing, sprzedaż oraz zarząd.

## Topologia Sieci

### Opis Sieci

W każdym z działów znajduje się router Cisco 2811 oraz switch multilayer switch 3650-24PS, regulujący przepływ danych w danej podsieci. Liczba urządzeń różni się między oddziałami.

## Działy i Ich Konfiguracja

### Dział 1 - Zarząd

- **VLAN 11 (Dane):** 192.168.11.0/24
- **VLAN 12 (VoiP):** 192.168.12.0/24
- **Połączenie Międzysieciowe:** 172.16.0.0/24
- **Port:** GigabitEthernet0/0/0
- **Zakres Numerów Telefonów:** 1001-1003
- **Ilość Telefonów:** 3
- **Możliwość Podpięcia Telefonów Maksymalnie:** 23

### Dział 2 - Sprzedaż

- **VLAN 9 (Dane):** 192.168.9.0/24
- **VLAN 10 (VoiP):** 192.168.10.0/24
- **Połączenie Międzysieciowe:** 172.16.0.0/24
- **Zakres Numerów Telefonów:** 2001-2008
- **Ilość Telefonów:** 8
- **Możliwość Podpięcia Telefonów Maksymalnie:** 21

### Dział 3 - Logistyka

- **VLAN 7 (Dane):** 192.168.7.0/24
- **VLAN 8 (VoiP):** 192.168.8.0/24
- **Połączenie Międzysieciowe:** 172.16.0.0/24
- **Zakres Numerów Telefonów:** 3001-3003
- **Ilość Telefonów:** 3
- **Możliwość Podpięcia Telefonów Maksymalnie:** 23

### Dział 4 - Marketing

- **VLAN 5 (Dane):** 192.168.5.0/24
- **VLAN 6 (VoiP):** 192.168.6.0/24
- **Połączenie Międzysieciowe:** 172.16.0.0/24
- **Zakres Numerów Telefonów:** 4001-4003
- **Ilość Telefonów:** 3
- **Możliwość Podpięcia Telefonów Maksymalnie:** 23

### Dział 5 - Księgowość

- **VLAN 3 (Dane):** 192.168.3.0/24
- **VLAN 4 (VoiP):** 192.168.4.0/24
- **Połączenie Międzysieciowe:** 172.16.0.0/24
- **Zakres Numerów Telefonów:** 5001-5003
- **Ilość Telefonów:** 3
- **Możliwość Podpięcia Telefonów Maksymalnie:** 22

## Etapy Konfiguracji Sieci Lokalnych

### 4.1 Konfiguracja Podstawowych Ustawień Urządzeń

- Pobieranie adresu IP na DHCP dla wszystkich komputerów.
- Konfiguracja adresu dla telefonów analogowych w module Home VoIP.

### 4.2 Konfiguracja Switchy Lokalnych

- Konfiguracja VLAN-ów zgodnie z przykładem dla Switcha Zarządu.

### 4.3 Konfiguracja Głównego Switcha

- Konfiguracja interfejsów i ich przypisanie do odpowiednich routerów i serwera.

### 4.4 Konfiguracja Routerów Lokalnych

- Konfiguracja DHCP dla danych oraz VoiP.
- Konfiguracja interfejsów dla danych i VoiP.
- Konfiguracja protokołu RIP i VoiP dla każdego routera.

### 4.5 Konfiguracja Routera Głównego

- Konfiguracja DHCP dla danych.
- Konfiguracja interfejsów dla danych i podłączenia do ISP.
- Konfiguracja protokołu RIP.

### 4.6 Konfiguracja Routera ISP

- Konfiguracja DHCP dla połączenia z ISP.
- Konfiguracja interfejsu dla połączenia z ISP.

## Kosztorys

| Ilość | Nazwa                               | Koszt za Sztukę | Koszt Całkowity |
|-------|-------------------------------------|-----------------|------------------|
| 1x    | Router 2901                         | 600 zł          | 600 zł           |
| 6x    | Router 2811                         | 700 zł          | 4 200 zł         |
| 1x    | Switch PT                           | 200 zł          | 200 zł           |
| 5x    | Switch 3650-24PS                    | 1300 zł         | 6 500 zł         |
| 18x   | Telefon IP Phone 7960               | 300 zł          | 5 400 zł         |
| 18x   | Komputer PC                         | 2000 zł         | 36 000 zł        |
| 2x    | Laptop                              | 2000 zł         | 4 000 zł         |
| 2x    | Jednostka Podstawowa Home VoIP      | 500 zł          | 1 000 zł         |
| 2x    | Telefon Analogowy                   | --              | --               |
| 7x    | PT-SWITCH-NM-1FGE                   | 142 zł          | 1 000 zł         |
| 18x   | HWIC-1GE-SFP                        | 944 zł          | 17 000 zł        |
| 18x   | GLC-LH-SMD                          | 138 zł          | 2 500
