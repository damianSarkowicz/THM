# 💻 Virtualisation Basics

> **Quick Summary:** Wprowadzenie do wirtualizacji i konteneryzacji, rola menedżera Hypervisor, kluczowe pojęcia (VM, Kontener, Porty) oraz korzyści z izolacji środowisk w IT i cyberbezpieczeństwie.

---

## 🔑 Kluczowe Pojęcia (Key Terminology)

### 1. Virtualization & Hypervisor
* **Virtualization (Wirtualizacja):** Technologia, która pozwala jednemu fizycznemu komputerowi działać tak, jakby był wieloma osobnymi komputerami.
* **Hypervisor:** Oprogramowanie zarządcze („menedżer”), które tworzy i uruchamia maszyny wirtualne na fizycznym sprzęcie.

### 2. Lab Machine / VM vs Container
* **Lab Machine / Virtual Machine (VM):** Cały wirtualny komputer uruchomiony wewnątrz fizycznej maszyny, posiadający własny, osobny system operacyjny.
* **Container (Kontener):** Mały, odizolowany „boks” dla jednej konkretnej aplikacji, który współdzieli ten sam system operacyjny z komputerem fizycznym (hostem).
* **Container Images (Obrazy Kontenerów):** Gotowy szablon lub „przepis”, na podstawie którego tworzone są kontenery.

### 3. Network Ports (Porty Sieciowe)
* **Porty:** Numerowane punkty wejścia, z których korzystają aplikacje, aby komunikować się między sobą przez sieć.

---

## 🚀 Główny Zalety Wirtualizacji (Key Benefits)

* **Safe testing for cyber security:** Bezpieczne testowanie programów i rozwiązań w odizolowanym środowisku, bez ryzyka dla głównego komputera.
* **Cost savings & Better resource usage:** Oszczędność pieniędzy i lepsze wykorzystanie zasobów sprzętowych.
* **Faster deployment:** Znacznie szybsze i łatwiejsze uruchamianie nowych aplikacji.
* **Flexibility & Portability:** Duża elastyczność i łatwość przenoszenia gotowych środowisk.
* **Scalability & Centralized Management:** Łatwe skalowanie oraz zarządzanie wszystkim z jednego miejsca.

---

## 📌 Podsumowanie w 3 zdaniach
1. Wirtualizacja pozwala uruchamiać wiele osobnych maszyn (**VM**) na jednym komputerze dzięki oprogramowaniu **Hypervisor**.
2. **Kontener** to lżejsza alternatywa dla maszyny wirtualnej, służąca do uruchomienia jednej aplikacji i współdzieląca system z hostem.
3. Wirtualizacja zapewnia bezpieczne środowisko testowe (**Safe testing**) i stanowi fundament pod technologię chmurową (**Cloud Computing**).

Wirtualizacja i konteneryzacja zapewniają szybki, bezpieczny i spójny sposób na uruchamianie aplikacji.