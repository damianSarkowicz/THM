# 🌐 Client-Server Basics & Web Communication

> **Quick Summary:** Podstawowy model komunikacji w sieci oparty na relacji Klient-Serwer, protokołach HTTP/HTTPS, analizie ruchu w przeglądarce (DevTools) oraz 9 głównych metodach HTTP.

---

## 🔑 Kluczowe Pojęcia

### 1. Client & Server (Klient i Serwer)
* **Client (Klient):** Urządzenie lub aplikacja, która **prosi o dane** (np. przeglądarka Chrome, klient SSH).
* **Server (Serwer):** Komputer, który stale działa, **nasłuchuje zapytań** i odsyła żądane zasoby.

### 2. Request & Response (Zapytanie i Odpowiedź)
* **Request (Zapytanie):** Klient mówi: *"Serwerze, daj mi stronę index.html"*.
* **Response (Odpowiedź):** Serwer odpowiada: *"Oto Twoja strona (200 OK)"* LUB *"Nie mam takiej strony (404 Not Found)"*.

### 3. Service (Usługa)
* Dedykowana aplikacja działająca na serwerze, odpowiadająca za konkretne zadanie.
* *Przykłady:* Serwer WWW (Apache/Nginx/Python SimpleHTTP), serwer poczty (SMTP), serwer bazy danych (MySQL).

---

## 🛠️ Mechanizmy Łączności & Identyfikacja

### 4. Protocol (Protokół)
* **Język komunikacji.** Zbiór reguł, dzięki którym klient i serwer rozumieją się nawzajem.
* **HTTP vs HTTPS:**
  * **HTTP:** Nie zapewnia szyfrowania przesyłanych danych. Komunikacja może być przechwycona i odczytana przez osobę mającą możliwość monitorowania ruchu.
  * **HTTPS (HTTP Secure):** Zabezpiecza komunikację HTTP za pomocą TLS, zapewniając m.in. poufność i integralność przesyłanych danych.

### 5. Port (Port sieciowy)
* **"Drzwi" na serwerze.** Numer od `0` do `65535`, który kieruje ruch do konkretnej usługi.
* **Ważne porty do zapamiętania:**
  * `80` → HTTP (zwykłe strony WWW)
  * `443` → HTTPS (szyfrowane strony WWW)
  * `22` → SSH (zdalny dostęp do konsoli)
  * `53` → DNS (tłumaczenie nazw)

### 6. DNS (Domain Name System)
* **Książka telefoniczna Internetu.**
* Zamienia nazwę czytelną dla człowieka (np. `tryhackme.com`) na adres IP czytelny dla komputera.

---

## 🔍 Web Communication in Practice (Developer Tools Analysis)

Podczas wysyłania zapytania HTTP przeglądarka i narzędzia programistyczne (**DevTools → Network Tab**) pozwalają na dokładną inspekcję komunikacji:

### 📊 Podstawowe Pola Żądania i Odpowiedzi
* **Scheme:** Użyty protokół (`http` lub `https`).
* **Host:** Nazwa domeny/serwera, do którego wysyłamy zapytanie (np. `httpdemo.local:8080`).
* **Filename:** Ścieżka do żądanego zasobu (np. `/`, który może odpowiadać stronie głównej `index.html`).
* **Remote Address:** Adres IP oraz port serwera, z którym przeglądarka faktycznie się komunikuje (np. `127.0.0.1:8080`).
* **Status:** Kod wyniku przetworzenia zapytania przez serwer (np. `200 OK`, `404 Not Found`).

### 📋 Przykładowe Nagłówki (Response Headers)
* **Content-Type:** Typ zwracanej zawartości (np. `text/html`, `image/png`).
* **Content-Length:** Rozmiar zwracanej odpowiedzi w bajtach.
* **Server:** Informacja o oprogramowaniu używanym przez serwer (np. `SimpleHTTP/0.6 Python/3.12.3`).

---

## ⚙️ Metody HTTP (HTTP Methods / Commands)

W praktyce i materiałach edukacyjnych często wyróżnia się 9 podstawowych metod HTTP, zdefiniowanych w dokumentach RFC:

* **GET:** Pobieranie/odczytywanie danych z serwera (np. wyświetlenie strony). Parametry często przekazywane są w adresie URL.
* **POST:** Przesyłanie nowych danych na serwer (np. formularze logowania, rejestracja).
* **PUT:** Nadpisywanie lub tworzenie całego zasobu pod wskazanym adresem.
* **DELETE:** Usuwanie wskazanego zasobu z serwera.
* **PATCH:** Częściowa modyfikacja zasobu (aktualizacja wybranych pól).
* **HEAD:** Pobieranie samych nagłówków (Headers) bez treści strony (używane do diagnostyki).
* **OPTIONS:** Sprawdzanie dostępnych metod i opcji komunikacji ze wskazanym serwerem.
* **CONNECT:** Ustanawianie tunelu do wskazanego serwera (np. przy komunikacji przez Proxy).
* **TRACE:** Odsyłanie otrzymanego żądania z powrotem do klienta (służy do testów diagnostycznych).

---

## 📌 Podsumowanie w 3 zdaniach
1. Klient pyta za pomocą metod HTTP (**GET**, **POST** itp.), a serwer odpowiada kodem statusu i danymi w modelu **Request-Response**.
2. **DNS** zamienia domenę na IP, a **Port** (np. 80/443) kieruje ruch do właściwej usługi na serwerze.
3. Narzędzia **DevTools (Network Tab)** umożliwiają analitykowi inspekcję nagłówków, parametrów oraz metod pod kątem diagnostyki i bezpieczeństwa.