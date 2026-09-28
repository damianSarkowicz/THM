# 🖥️ Operating Systems Introduction

> **Quick Summary:** Wprowadzenie do systemów operacyjnych, ich rola w zarządzaniu sprzętem i aplikacjami, podział na Kernel Space i User Space, mechanizmy bezpieczeństwa, interfejsy (GUI vs CLI) oraz przegląd środowisk OS (Desktop, Server, Mobile, Cloud/Containers).

---

## 🔑 Kluczowe Pojęcia i Rola OS (Key Terminology)

### 1. Czym jest System Operacyjny (Operating System)?
* **Operating System (OS):** Główny program zarządzający zasobami sprzętowymi komputera, pamięcią, procesami oraz stanowiący platformę uruchomieniową dla aplikacji.

---

## 🛡️ Poziomy Uprawnień i Zadania OS (Privilege Layers & OS Duties)

### 1. Podział na Przestrzenie Uprawnień (System Privilege Layers)
* **Kernel Space (Przestrzeń Jądra):** Uprzywilejowana i chroniona przestrzeń systemu operacyjnego, w której działa kernel. Ma bezpośredni dostęp do CPU, pamięci, pamięci masowej i sprzętu oraz zarządza zasobami systemu.
* **User Space (Przestrzeń Użytkownika):** Przestrzeń, w której działają standardowe aplikacje z ograniczonymi uprawnieniami. Aplikacje nie mogą bezpośrednio korzystać ze sprzętu - gdy potrzebują wykonać operację wymagającą uprawnień, korzystają z system calls, prosząc kernel o jej wykonanie.

### 2. Obowiązki Systemu Operacyjnego (OS Duties)
* **Process Management:** Tworzenie, planowanie (scheduling), wykonywanie i kończenie procesów oraz zarządzanie ich zasobami.
* **Memory Management:** Kontrola i przydzielanie pamięci RAM (pamięć wirtualna) dla poszczególnych aplikacji.
* **File System Management:** Organizacja, odczyt i zapis danych na pamięci masowej w formie struktury plików i katalogów.
* **Device Management:** Komunikacja ze sprzętem zewnętrznym za pomocą sterowników (drivers) oraz obsługa urządzeń wejścia/wyjścia (I/O).
* **User Management:** Tworzenie i obsługa kont użytkowników, zarządzanie grupami oraz egzekwowanie uprawnień dostępu do systemu.

---

## 🔒 Bezpieczeństwo w Systemie Operacyjnym (OS Security)

System operacyjny dba o ochronę zasobów i izolację użytkowników poprzez:
* **Authentication (Uwierzytelnianie):** Weryfikacja tożsamości użytkownika przed udzieleniem dostępu (hasła, biometria, klucze).
* **Permissions (Uprawnienia):** Kontrola dostępu do plików i procesów (np. odczyt, zapis, wykonanie — Read/Write/Execute).
* **Isolation (Izolacja):** Separacja procesów w pamięci, która domyślnie uniemożliwia jednemu procesowi dostęp do pamięci innego procesu bez odpowiednich uprawnień.
* **System Protection:** Zabezpieczenie krytycznych obszarów jądra przed modyfikacją z poziomu User Space.

---

## 🖥️ Interfejsy i Krajobraz Systemów (OS Interfaces & Landscape)

### 1. Interfejsy Użytkownika (OS Interfaces)
* **GUI (Graphical User Interface):** Graficzny interfejs oparty na oknach, ikonach i menu, obsługiwany myszką lub dotykiem (łatwy w użyciu).
* **CLI (Command-Line Interface):** Tekstowy interfejs, w którym polecenia wpisuje się ręcznie. Zapewnia wyższą precyzję, szybsze działanie oraz możliwość automatyzacji (skrypty).

### 2. Typy Systemów Operacyjnych i Zastosowanie (OS Landscape)
Różne urządzenia i środowiska wymagają odmiennych funkcji od systemu operacyjnego:

| Kategoria | Przykłady OS | Charakterystyka i Zastosowanie |
| :--- | :--- | :--- |
| **Desktop** | Windows 11, macOS, Linux (Ubuntu) | Nastawione na wygodę użytkownika, bogaty interfejs GUI i obsługę wielu aplikacji użytkowych. |
| **Server** | Windows Server, Red Hat (RHEL), Ubuntu Server | Zoptymalizowane pod kątem wydajności, stabilności i pracy wieloużytkownikowej; często bez GUI (headless). |
| **Mobile** | Android, iOS | Energooszczędne, zoptymalizowane pod ekrany dotykowe, łączność bezprzewodową i izolację aplikacji (sandboxing). |
| **Embedded & IoT** | Embedded Linux, FreeRTOS | Minimalistyczne systemy wbudowane w urządzenia (np. routery, agd, czujniki) o bardzo małym zużyciu zasobów. |
| **Virtual & Cloud** | Amazon Linux, Ubuntu LTS | Dostosowane do pracy na wirtualnych maszynach w chmurze z łatwym skalowaniem. |

> **Dlaczego istnieje tyle wersji?** Różne środowiska mają odmienne wymagania dotyczące wydajności, bezpieczeństwa, poboru prądu oraz wsparcia dla konkretnego sprzętu.

---

## 📌 Podsumowanie w 3 zdaniach
1. System operacyjny (OS) zarządza sprzętem, pamięcią, plikami oraz użytkownikami, pośrednicząc między fizyczną maszyną a aplikacjami.
2. Podział na **Kernel Space** (wysokie uprawnienia) i **User Space** (izolacja aplikacji) oraz mechanizmy kontroli dostępu zapewniają stabilność i bezpieczeństwo całego systemu.
3. Różnorodność systemów - od desktopowych (**Windows**, **Linux**), przez serwerowe i chmurowe, po zoptymalizowane pod kontenery (**Alpine**, **Bottlerocket**) - wynika z odmiennych wymagań sprzętowych i środowiskowych.

### System operacyjny stanowi kluczowy fundament zarządzania zasobami i bezpieczeństwem w każdym środowisku IT.